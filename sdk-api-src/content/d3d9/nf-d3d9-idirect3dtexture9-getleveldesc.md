---
UID: NF:d3d9.IDirect3DTexture9.GetLevelDesc
title: IDirect3DTexture9::GetLevelDesc (d3d9.h)
description: The IDirect3DTexture9::GetLevelDesc (d3d9.h) method retrieves a level description of a texture resource.
helpviewer_keywords: ["56fc4d84-d125-0b2e-6670-ecb45faa49cd","GetLevelDesc","GetLevelDesc method [Direct3D 9]","GetLevelDesc method [Direct3D 9]","IDirect3DTexture9 interface","IDirect3DTexture9 interface [Direct3D 9]","GetLevelDesc method","IDirect3DTexture9.GetLevelDesc","IDirect3DTexture9::GetLevelDesc","d3d9helper/IDirect3DTexture9::GetLevelDesc","direct3d9.idirect3dtexture9__getleveldesc"]
old-location: direct3d9\idirect3dtexture9__getleveldesc.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dtexture9__getleveldesc.htm
ms.date: 08/11/2022
ms.keywords: 56fc4d84-d125-0b2e-6670-ecb45faa49cd, GetLevelDesc, GetLevelDesc method [Direct3D 9], GetLevelDesc method [Direct3D 9],IDirect3DTexture9 interface, IDirect3DTexture9 interface [Direct3D 9],GetLevelDesc method, IDirect3DTexture9.GetLevelDesc, IDirect3DTexture9::GetLevelDesc, d3d9helper/IDirect3DTexture9::GetLevelDesc, direct3d9.idirect3dtexture9__getleveldesc
req.header: d3d9.h
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
 - IDirect3DTexture9::GetLevelDesc
 - d3d9/IDirect3DTexture9::GetLevelDesc
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
 - IDirect3DTexture9.GetLevelDesc
---

# IDirect3DTexture9::GetLevelDesc


## -description

Retrieves a level description of a texture resource.

## -parameters

### -param Level [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Identifies a level of the texture resource. This method returns a surface description for the level specified by this parameter.

### -param pDesc [out]

Type: <b><a href="/windows/desktop/direct3d9/d3dsurface-desc">D3DSURFACE_DESC</a>*</b>

Pointer to a <a href="/windows/desktop/direct3d9/d3dsurface-desc">D3DSURFACE_DESC</a> structure, describing the returned level.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. D3DERR_INVALIDCALL is returned if one of the arguments is invalid.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dtexture9">IDirect3DTexture9</a>
