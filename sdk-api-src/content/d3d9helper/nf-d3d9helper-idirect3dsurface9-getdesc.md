---
UID: NF:d3d9helper.IDirect3DSurface9.GetDesc
title: IDirect3DSurface9::GetDesc (d3d9helper.h)
description: The IDirect3DSurface9::GetDesc method (d3d9helper.h) retrieves a description of the surface.
helpviewer_keywords: ["068aa9b6-08d4-5e72-dc9f-18e83e42aef2","GetDesc","GetDesc method [Direct3D 9]","GetDesc method [Direct3D 9]","IDirect3DSurface9 interface","IDirect3DSurface9 interface [Direct3D 9]","GetDesc method","IDirect3DSurface9.GetDesc","IDirect3DSurface9::GetDesc","d3d9helper/IDirect3DSurface9::GetDesc","direct3d9.idirect3dsurface9__getdesc"]
old-location: direct3d9\idirect3dsurface9__getdesc.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dsurface9__getdesc.htm
ms.date: 08/11/2022
ms.keywords: 068aa9b6-08d4-5e72-dc9f-18e83e42aef2, GetDesc, GetDesc method [Direct3D 9], GetDesc method [Direct3D 9],IDirect3DSurface9 interface, IDirect3DSurface9 interface [Direct3D 9],GetDesc method, IDirect3DSurface9.GetDesc, IDirect3DSurface9::GetDesc, d3d9helper/IDirect3DSurface9::GetDesc, direct3d9.idirect3dsurface9__getdesc
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
 - IDirect3DSurface9::GetDesc
 - d3d9helper/IDirect3DSurface9::GetDesc
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
 - IDirect3DSurface9.GetDesc
---

# IDirect3DSurface9::GetDesc


## -description

Retrieves a description of the surface.

## -parameters

### -param pDesc [out]

Type: <b><a href="/windows/desktop/direct3d9/d3dsurface-desc">D3DSURFACE_DESC</a>*</b>

Pointer to a <a href="/windows/desktop/direct3d9/d3dsurface-desc">D3DSURFACE_DESC</a> structure, describing the surface.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK.

D3DERR_INVALIDCALL is returned if the argument is invalid.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a>
