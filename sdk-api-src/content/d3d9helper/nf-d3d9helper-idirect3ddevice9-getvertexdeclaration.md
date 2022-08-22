---
UID: NF:d3d9helper.IDirect3DDevice9.GetVertexDeclaration
title: IDirect3DDevice9::GetVertexDeclaration (d3d9helper.h)
description: The IDirect3DDevice9::GetVertexDeclaration method (d3d9.h) gets a vertex shader declaration.
helpviewer_keywords: ["8b909692-06a8-7089-4aa2-4693ff481d81","GetVertexDeclaration","GetVertexDeclaration method [Direct3D 9]","GetVertexDeclaration method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","GetVertexDeclaration method","IDirect3DDevice9.GetVertexDeclaration","IDirect3DDevice9::GetVertexDeclaration","d3d9helper/IDirect3DDevice9::GetVertexDeclaration","direct3d9.idirect3ddevice9__getvertexdeclaration"]
old-location: direct3d9\idirect3ddevice9__getvertexdeclaration.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getvertexdeclaration.htm
ms.date: 08/11/2022
ms.keywords: 8b909692-06a8-7089-4aa2-4693ff481d81, GetVertexDeclaration, GetVertexDeclaration method [Direct3D 9], GetVertexDeclaration method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetVertexDeclaration method, IDirect3DDevice9.GetVertexDeclaration, IDirect3DDevice9::GetVertexDeclaration, d3d9helper/IDirect3DDevice9::GetVertexDeclaration, direct3d9.idirect3ddevice9__getvertexdeclaration
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
 - IDirect3DDevice9::GetVertexDeclaration
 - d3d9helper/IDirect3DDevice9::GetVertexDeclaration
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
 - IDirect3DDevice9.GetVertexDeclaration
---

# IDirect3DDevice9::GetVertexDeclaration


## -description

Gets a vertex shader declaration.

## -parameters

### -param ppDecl [out]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvertexdeclaration9">IDirect3DVertexDeclaration9</a>**</b>

Pointer to an <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvertexdeclaration9">IDirect3DVertexDeclaration9</a> object that is returned.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK.
 The return value can be D3DERR_INVALIDCALL.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexdeclaration">IDirect3DDevice9::SetVertexDeclaration</a>
