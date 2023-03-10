---
UID: NF:d3d9.IDirect3DVolumeTexture9.UnlockBox
title: IDirect3DVolumeTexture9::UnlockBox (d3d9.h)
description: The IDirect3DVolumeTexture9::UnlockBox (d3d9.h) method unlocks a box on a volume texture resource.
helpviewer_keywords: ["5b89d036-c0de-c93d-6c62-1b4072dc95c7","IDirect3DVolumeTexture9 interface [Direct3D 9]","UnlockBox method","IDirect3DVolumeTexture9.UnlockBox","IDirect3DVolumeTexture9::UnlockBox","UnlockBox","UnlockBox method [Direct3D 9]","UnlockBox method [Direct3D 9]","IDirect3DVolumeTexture9 interface","d3d9helper/IDirect3DVolumeTexture9::UnlockBox","direct3d9.idirect3dvolumetexture9__unlockbox"]
old-location: direct3d9\idirect3dvolumetexture9__unlockbox.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dvolumetexture9__unlockbox.htm
ms.date: 08/11/2022
ms.keywords: 5b89d036-c0de-c93d-6c62-1b4072dc95c7, IDirect3DVolumeTexture9 interface [Direct3D 9],UnlockBox method, IDirect3DVolumeTexture9.UnlockBox, IDirect3DVolumeTexture9::UnlockBox, UnlockBox, UnlockBox method [Direct3D 9], UnlockBox method [Direct3D 9],IDirect3DVolumeTexture9 interface, d3d9helper/IDirect3DVolumeTexture9::UnlockBox, direct3d9.idirect3dvolumetexture9__unlockbox
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
 - IDirect3DVolumeTexture9::UnlockBox
 - d3d9/IDirect3DVolumeTexture9::UnlockBox
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
 - IDirect3DVolumeTexture9.UnlockBox
---

# IDirect3DVolumeTexture9::UnlockBox


## -description

Unlocks a box on a volume texture resource.

## -parameters

### -param Level [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Specifies the level of the volume texture resource to unlock.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9">IDirect3DVolumeTexture9</a>



<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-lockbox">LockBox</a>
