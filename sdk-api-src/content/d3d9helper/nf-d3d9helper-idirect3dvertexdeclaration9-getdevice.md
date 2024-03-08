---
UID: NF:d3d9helper.IDirect3DVertexDeclaration9.GetDevice
title: IDirect3DVertexDeclaration9::GetDevice (d3d9helper.h)
description: The IDirect3DVertexDeclaration9::GetDevice method (d3d9helper.h) gets the current device.
helpviewer_keywords: ["06ae2ca9-697f-c95d-8f0b-7e78f6bb21dd","GetDevice","GetDevice method [Direct3D 9]","GetDevice method [Direct3D 9]","IDirect3DVertexDeclaration9 interface","IDirect3DVertexDeclaration9 interface [Direct3D 9]","GetDevice method","IDirect3DVertexDeclaration9.GetDevice","IDirect3DVertexDeclaration9::GetDevice","d3d9helper/IDirect3DVertexDeclaration9::GetDevice","direct3d9.idirect3dvertexdeclaration9__getdevice"]
old-location: direct3d9\idirect3dvertexdeclaration9__getdevice.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dvertexdeclaration9__getdevice.htm
ms.date: 08/12/2022
ms.keywords: 06ae2ca9-697f-c95d-8f0b-7e78f6bb21dd, GetDevice, GetDevice method [Direct3D 9], GetDevice method [Direct3D 9],IDirect3DVertexDeclaration9 interface, IDirect3DVertexDeclaration9 interface [Direct3D 9],GetDevice method, IDirect3DVertexDeclaration9.GetDevice, IDirect3DVertexDeclaration9::GetDevice, d3d9helper/IDirect3DVertexDeclaration9::GetDevice, direct3d9.idirect3dvertexdeclaration9__getdevice
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
 - IDirect3DVertexDeclaration9::GetDevice
 - d3d9helper/IDirect3DVertexDeclaration9::GetDevice
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
 - IDirect3DVertexDeclaration9.GetDevice
---

# IDirect3DVertexDeclaration9::GetDevice


## -description

Gets the current device.

## -parameters

### -param ppDevice [out, retval]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>**</b>

Pointer to the IDirect3DDevice9 interface that is returned.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be:
     D3DERR_INVALIDCALL.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvertexdeclaration9">IDirect3DVertexDeclaration9</a>
