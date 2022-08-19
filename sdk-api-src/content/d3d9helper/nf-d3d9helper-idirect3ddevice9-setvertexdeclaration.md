---
UID: NF:d3d9helper.IDirect3DDevice9.SetVertexDeclaration
title: IDirect3DDevice9::SetVertexDeclaration (d3d9helper.h)
description: The IDirect3DDevice9::SetVertexDeclaration method (d3d9helper.h) sets a Vertex Declaration (Direct3D 9).
helpviewer_keywords: ["12796c02-d1b4-5f9d-8414-04b978887c2a","IDirect3DDevice9 interface [Direct3D 9]","SetVertexDeclaration method","IDirect3DDevice9.SetVertexDeclaration","IDirect3DDevice9::SetVertexDeclaration","SetVertexDeclaration","SetVertexDeclaration method [Direct3D 9]","SetVertexDeclaration method [Direct3D 9]","IDirect3DDevice9 interface","d3d9helper/IDirect3DDevice9::SetVertexDeclaration","direct3d9.idirect3ddevice9__setvertexdeclaration"]
old-location: direct3d9\idirect3ddevice9__setvertexdeclaration.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setvertexdeclaration.htm
ms.date: 08/11/2022
ms.keywords: 12796c02-d1b4-5f9d-8414-04b978887c2a, IDirect3DDevice9 interface [Direct3D 9],SetVertexDeclaration method, IDirect3DDevice9.SetVertexDeclaration, IDirect3DDevice9::SetVertexDeclaration, SetVertexDeclaration, SetVertexDeclaration method [Direct3D 9], SetVertexDeclaration method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::SetVertexDeclaration, direct3d9.idirect3ddevice9__setvertexdeclaration
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
 - IDirect3DDevice9::SetVertexDeclaration
 - d3d9helper/IDirect3DDevice9::SetVertexDeclaration
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
 - IDirect3DDevice9.SetVertexDeclaration
---

# IDirect3DDevice9::SetVertexDeclaration


## -description

Sets a <a href="/windows/desktop/direct3d9/vertex-declaration">Vertex Declaration (Direct3D 9)</a>.

## -parameters

### -param pDecl [in]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvertexdeclaration9">IDirect3DVertexDeclaration9</a>*</b>

Pointer to an <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvertexdeclaration9">IDirect3DVertexDeclaration9</a> object, which contains the vertex declaration.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK.
 The return value can be D3DERR_INVALIDCALL.

## -remarks

A vertex declaration is an IDirect3DVertexDeclaration9 object that defines the data members of a vertex (i.e. texture coordinates, colors, normals, etc.). This data can be useful for implementing <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-pguide">vertex shaders and pixel shaders</a>.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getvertexdeclaration">IDirect3DDevice9::GetVertexDeclaration</a>
