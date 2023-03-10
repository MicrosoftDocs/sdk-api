---
UID: NF:d3d9.IDirect3DTexture9.UnlockRect
title: IDirect3DTexture9::UnlockRect (d3d9.h)
description: The IDirect3DTexture9::UnlockRect (d3d9.h) method unlocks a rectangle on a texture resource.
helpviewer_keywords: ["IDirect3DTexture9 interface [Direct3D 9]","UnlockRect method","IDirect3DTexture9.UnlockRect","IDirect3DTexture9::UnlockRect","UnlockRect","UnlockRect method [Direct3D 9]","UnlockRect method [Direct3D 9]","IDirect3DTexture9 interface","d3d9helper/IDirect3DTexture9::UnlockRect","dc06fd43-b5ef-87a2-a68e-2779288b756b","direct3d9.idirect3dtexture9__unlockrect"]
old-location: direct3d9\idirect3dtexture9__unlockrect.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dtexture9__unlockrect.htm
ms.date: 08/11/2022
ms.keywords: IDirect3DTexture9 interface [Direct3D 9],UnlockRect method, IDirect3DTexture9.UnlockRect, IDirect3DTexture9::UnlockRect, UnlockRect, UnlockRect method [Direct3D 9], UnlockRect method [Direct3D 9],IDirect3DTexture9 interface, d3d9helper/IDirect3DTexture9::UnlockRect, dc06fd43-b5ef-87a2-a68e-2779288b756b, direct3d9.idirect3dtexture9__unlockrect
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
 - IDirect3DTexture9::UnlockRect
 - d3d9/IDirect3DTexture9::UnlockRect
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
 - IDirect3DTexture9.UnlockRect
---

# IDirect3DTexture9::UnlockRect


## -description

Unlocks a rectangle on a texture resource.

## -parameters

### -param Level [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Specifies the level of the texture resource to unlock.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dtexture9">IDirect3DTexture9</a>



<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-lockrect">IDirect3DTexture9::LockRect</a>
