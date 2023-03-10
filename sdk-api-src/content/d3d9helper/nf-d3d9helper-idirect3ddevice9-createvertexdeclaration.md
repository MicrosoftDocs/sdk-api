---
UID: NF:d3d9helper.IDirect3DDevice9.CreateVertexDeclaration
title: IDirect3DDevice9::CreateVertexDeclaration (d3d9helper.h)
description: The IDirect3DDevice9::CreateVertexDeclaration method (d3d9helper.h) creates a vertex shader declaration from the device and the vertex elements.
helpviewer_keywords: ["CreateVertexDeclaration","CreateVertexDeclaration method [Direct3D 9]","CreateVertexDeclaration method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","CreateVertexDeclaration method","IDirect3DDevice9.CreateVertexDeclaration","IDirect3DDevice9::CreateVertexDeclaration","d3d9helper/IDirect3DDevice9::CreateVertexDeclaration","direct3d9.idirect3ddevice9__createvertexdeclaration","fcad3843-471b-7e52-ff9d-c4cb3cf5da52"]
old-location: direct3d9\idirect3ddevice9__createvertexdeclaration.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__createvertexdeclaration.htm
ms.date: 08/11/2022
ms.keywords: CreateVertexDeclaration, CreateVertexDeclaration method [Direct3D 9], CreateVertexDeclaration method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],CreateVertexDeclaration method, IDirect3DDevice9.CreateVertexDeclaration, IDirect3DDevice9::CreateVertexDeclaration, d3d9helper/IDirect3DDevice9::CreateVertexDeclaration, direct3d9.idirect3ddevice9__createvertexdeclaration, fcad3843-471b-7e52-ff9d-c4cb3cf5da52
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
 - IDirect3DDevice9::CreateVertexDeclaration
 - d3d9helper/IDirect3DDevice9::CreateVertexDeclaration
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
 - IDirect3DDevice9.CreateVertexDeclaration
---

# IDirect3DDevice9::CreateVertexDeclaration


## -description

Create a vertex shader declaration from the device and the vertex elements.

## -parameters

### -param pVertexElements [in]

Type: <b>const <a href="/windows/desktop/direct3d9/d3dvertexelement9">D3DVERTEXELEMENT9</a>*</b>

An array of <a href="/windows/desktop/direct3d9/d3dvertexelement9">D3DVERTEXELEMENT9</a> vertex elements.

### -param ppDecl [out, retval]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvertexdeclaration9">IDirect3DVertexDeclaration9</a>**</b>

Pointer to an <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvertexdeclaration9">IDirect3DVertexDeclaration9</a> pointer that returns the created vertex shader declaration.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be
     D3DERR_INVALIDCALL.

## -remarks

See the <a href="/windows/desktop/direct3d9/vertex-declaration">Vertex Declaration (Direct3D 9)</a> page for a detailed description of how to map vertex declarations between different versions of DirectX.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>
