---
UID: NF:d3d9.IDirect3DCubeTexture9.AddDirtyRect
title: IDirect3DCubeTexture9::AddDirtyRect (d3d9.h)
description: The IDirect3DCubeTexture9::AddDirtyRect adds a dirty region to a cube texture resource. 
helpviewer_keywords: ["AddDirtyRect","AddDirtyRect method [Direct3D 9]","AddDirtyRect method [Direct3D 9]","IDirect3DCubeTexture9 interface","IDirect3DCubeTexture9 interface [Direct3D 9]","AddDirtyRect method","IDirect3DCubeTexture9.AddDirtyRect","IDirect3DCubeTexture9::AddDirtyRect","b0dc98c8-8a1a-85fb-09ae-35df9bd8edc0","d3d9helper/IDirect3DCubeTexture9::AddDirtyRect","direct3d9.idirect3dcubetexture9__adddirtyrect"]
old-location: direct3d9\idirect3dcubetexture9__adddirtyrect.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dcubetexture9__adddirtyrect.htm
ms.date: 08/10/2022
ms.keywords: AddDirtyRect, AddDirtyRect method [Direct3D 9], AddDirtyRect method [Direct3D 9],IDirect3DCubeTexture9 interface, IDirect3DCubeTexture9 interface [Direct3D 9],AddDirtyRect method, IDirect3DCubeTexture9.AddDirtyRect, IDirect3DCubeTexture9::AddDirtyRect, b0dc98c8-8a1a-85fb-09ae-35df9bd8edc0, d3d9helper/IDirect3DCubeTexture9::AddDirtyRect, direct3d9.idirect3dcubetexture9__adddirtyrect
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
 - IDirect3DCubeTexture9::AddDirtyRect
 - d3d9/IDirect3DCubeTexture9::AddDirtyRect
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
 - IDirect3DCubeTexture9.AddDirtyRect
---

# IDirect3DCubeTexture9::AddDirtyRect


## -description

Adds a dirty region to a cube texture resource.

## -parameters

### -param FaceType [in]

Type: <b><a href="/windows/desktop/direct3d9/d3dcubemap-faces">D3DCUBEMAP_FACES</a></b>

Member of the <a href="/windows/desktop/direct3d9/d3dcubemap-faces">D3DCUBEMAP_FACES</a> enumerated type, identifying the cube map face.

### -param pDirtyRect [in]

Type: <b>const <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure, specifying the dirty region. Specifying <b>NULL</b> expands the dirty region to cover the entire cube texture.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be: D3DERR_INVALIDCALL.

## -remarks

For performance reasons, dirty regions are only recorded for level zero of a texture. For sublevels, it is assumed that the corresponding (scaled) rectangle or box is also dirty. Dirty regions are automatically recorded when <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3dcubetexture9-lockrect">IDirect3DCubeTexture9::LockRect</a> is called without <a href="/windows/desktop/direct3d9/d3dlock">D3DLOCK_NO_DIRTY_UPDATE</a> or <a href="/windows/desktop/direct3d9/d3dlock">D3DLOCK_READONLY</a>. The destination surface of <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatesurface">IDirect3DDevice9::UpdateSurface</a> is also marked dirty automatically.

Using <a href="/windows/desktop/direct3d9/d3dlock">D3DLOCK_NO_DIRTY_UPDATE</a> and explicitly specifying dirty regions can be used to increase the efficiency of <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatetexture">IDirect3DDevice9::UpdateTexture</a>. Using this method, applications can optimize what subset of a resource is copied by specifying dirty regions on the resource. However, the dirty regions may be expanded to optimize alignment.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9">IDirect3DCubeTexture9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3dcubetexture9-getleveldesc">IDirect3DCubeTexture9::GetLevelDesc</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3dcubetexture9-lockrect">IDirect3DCubeTexture9::LockRect</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3dcubetexture9-unlockrect">IDirect3DCubeTexture9::UnlockRect</a>
