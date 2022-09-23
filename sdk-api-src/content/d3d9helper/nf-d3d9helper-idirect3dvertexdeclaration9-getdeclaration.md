---
UID: NF:d3d9helper.IDirect3DVertexDeclaration9.GetDeclaration
title: IDirect3DVertexDeclaration9::GetDeclaration (d3d9helper.h)
description: The IDirect3DVertexDeclaration9::GetDeclaration method (d3d9helper.h) gets the vertex shader declaration.
helpviewer_keywords: ["GetDeclaration","GetDeclaration method [Direct3D 9]","GetDeclaration method [Direct3D 9]","IDirect3DVertexDeclaration9 interface","IDirect3DVertexDeclaration9 interface [Direct3D 9]","GetDeclaration method","IDirect3DVertexDeclaration9.GetDeclaration","IDirect3DVertexDeclaration9::GetDeclaration","bd1cb4cd-85cf-525d-1ac3-ebd3eb527b1a","d3d9helper/IDirect3DVertexDeclaration9::GetDeclaration","direct3d9.idirect3dvertexdeclaration9__getdeclaration"]
old-location: direct3d9\idirect3dvertexdeclaration9__getdeclaration.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dvertexdeclaration9__getdeclaration.htm
ms.date: 08/12/2022
ms.keywords: GetDeclaration, GetDeclaration method [Direct3D 9], GetDeclaration method [Direct3D 9],IDirect3DVertexDeclaration9 interface, IDirect3DVertexDeclaration9 interface [Direct3D 9],GetDeclaration method, IDirect3DVertexDeclaration9.GetDeclaration, IDirect3DVertexDeclaration9::GetDeclaration, bd1cb4cd-85cf-525d-1ac3-ebd3eb527b1a, d3d9helper/IDirect3DVertexDeclaration9::GetDeclaration, direct3d9.idirect3dvertexdeclaration9__getdeclaration
req.header: d3d9helper.h
req.include-header: D3D9.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3D9.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirect3DVertexDeclaration9::GetDeclaration
 - d3d9helper/IDirect3DVertexDeclaration9::GetDeclaration
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DVertexDeclaration9.GetDeclaration
---

## -description

Gets the vertex shader declaration.

## -parameters

### -param pElement

Type: [in, out] <b><a href="/windows/desktop/direct3d9/d3dvertexelement9">D3DVERTEXELEMENT9</a>*</b>

Array of vertex elements (see <a href="/windows/desktop/direct3d9/d3dvertexelement9">D3DVERTEXELEMENT9</a>) that make up a vertex shader declaration. The application needs to allocate enough room for this. The vertex element array ends with the <a href="/windows/desktop/direct3d9/d3ddecl-end">D3DDECL_END</a> macro.

### -param pNumElements

Type: [out] <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

Number of elements in the array. The application needs to allocate enough room for this.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.

## -remarks

The number of elements, pNumElements, includes the <a href="/windows/desktop/direct3d9/d3ddecl-end">D3DDECL_END</a> macro, which ends the declaration. So the element count is actually one higher than the number of valid vertex elements.

Here's an example that will return the vertex declaration array of up to 256 elements:

```cpp
D3DVERTEXELEMENT9 decl[MAXD3DDECLLENGTH];
UINT numElements;
HRESULT hr = m_pVertexDeclaration->GetDeclaration( decl, &numElements);
```

Specify <b>NULL</b> for pDeclto get the number of elements in the declaration.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvertexdeclaration9">IDirect3DVertexDeclaration9</a>
