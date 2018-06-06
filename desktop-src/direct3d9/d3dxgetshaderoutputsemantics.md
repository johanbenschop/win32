---
Description: Get the semantics for all shader output elements.
ms.assetid: 1a3cdd5d-0ea7-48ae-a3f1-030e95b03a42
title: D3DXGetShaderOutputSemantics function
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# D3DXGetShaderOutputSemantics function

Get the semantics for all shader output elements.

## Syntax


```C++
HRESULT D3DXGetShaderOutputSemantics(
  _In_  const DWORD        *pFunction,
  _In_        D3DXSEMANTIC *pSemantics,
  _Out_       UINT         *pCount
);
```



## Parameters

<dl> <dt>

*pFunction* \[in\]
</dt> <dd>

Type: **const [**DWORD**](https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46)\***

Pointer to the shader function DWORD stream.

</dd> <dt>

*pSemantics* \[in\]
</dt> <dd>

Type: **[**D3DXSEMANTIC**](d3dxsemantic.md)\***

Pointer to an array of [**D3DXSEMANTIC**](d3dxsemantic.md) structures. The function will fill this array with the semantics for each output element referenced by the shader. This array is assumed to contain at least MAXD3DDECLLENGTH elements. However, calling **D3DXGetShaderOutputSemantics** with pSemantics = **NULL** will return the number of elements needed for pCount.

</dd> <dt>

*pCount* \[out\]
</dt> <dd>

Type: **[**UINT**](https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46)\***

Returns the number of elements in pSemantics.

</dd> </dl>

## Return value

Type: **[**HRESULT**](https://msdn.microsoft.com/windows/desktop/455d07e9-52c3-4efb-a9dc-2955cbfd38cc)**

If the function succeeds, the return value is D3D\_OK. If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.

## Requirements



|                    |                                                                                          |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Library<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## See also

<dl> <dt>

[Shader Functions](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 



