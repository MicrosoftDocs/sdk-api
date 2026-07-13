---
UID: NF:d3d9helper.IDirect3DCubeTexture9.UnlockRect
title: IDirect3DCubeTexture9::UnlockRect (d3d9helper.h)
description: The IDirect3DCubeTexture9::UnlockRect method (d3d9.h) unlocks a rectangle on a cube texture resource.
helpviewer_keywords: ["IDirect3DCubeTexture9 interface [Direct3D 9]","UnlockRect method","IDirect3DCubeTexture9.UnlockRect","IDirect3DCubeTexture9::UnlockRect","UnlockRect","UnlockRect method [Direct3D 9]","UnlockRect method [Direct3D 9]","IDirect3DCubeTexture9 interface","d3d9helper/IDirect3DCubeTexture9::UnlockRect","direct3d9.idirect3dcubetexture9__unlockrect","f5fb42b3-5c6a-7e4c-83fd-575e49595447"]
old-location: direct3d9\idirect3dcubetexture9__unlockrect.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dcubetexture9__unlockrect.htm
ms.date: 08/11/2022
ms.keywords: IDirect3DCubeTexture9 interface [Direct3D 9],UnlockRect method, IDirect3DCubeTexture9.UnlockRect, IDirect3DCubeTexture9::UnlockRect, UnlockRect, UnlockRect method [Direct3D 9], UnlockRect method [Direct3D 9],IDirect3DCubeTexture9 interface, d3d9helper/IDirect3DCubeTexture9::UnlockRect, direct3d9.idirect3dcubetexture9__unlockrect, f5fb42b3-5c6a-7e4c-83fd-575e49595447
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
 - IDirect3DCubeTexture9::UnlockRect
 - d3d9helper/IDirect3DCubeTexture9::UnlockRect
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
 - IDirect3DCubeTexture9.UnlockRect
---

# IDirect3DCubeTexture9::UnlockRect


## -description

Unlocks a rectangle on a cube texture resource.

## -parameters

### -param FaceType [in]

Type: <b><a href="/windows/desktop/direct3d9/d3dcubemap-faces">D3DCUBEMAP_FACES</a></b>

Member of the <a href="/windows/desktop/direct3d9/d3dcubemap-faces">D3DCUBEMAP_FACES</a> enumerated type, identifying a cube map face.

### -param Level [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Specifies a level of a mipmapped cube texture.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be: D3DERR_INVALIDCALL.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9">IDirect3DCubeTexture9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3dcubetexture9-adddirtyrect">IDirect3DCubeTexture9::AddDirtyRect</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3dcubetexture9-lockrect">IDirect3DCubeTexture9::LockRect</a>
