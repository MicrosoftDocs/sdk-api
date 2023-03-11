---
UID: NF:d3d9helper.IDirect3DCubeTexture9.LockRect
title: IDirect3DCubeTexture9::LockRect (d3d9helper.h)
description: The IDirect3DCubeTexture9::LockRect method (d3d9.h) locks a rectangle on a cube texture resource.
helpviewer_keywords: ["1f5618d3-63b7-c0fc-9b6e-44b99c39650c","IDirect3DCubeTexture9 interface [Direct3D 9]","LockRect method","IDirect3DCubeTexture9.LockRect","IDirect3DCubeTexture9::LockRect","LockRect","LockRect method [Direct3D 9]","LockRect method [Direct3D 9]","IDirect3DCubeTexture9 interface","d3d9helper/IDirect3DCubeTexture9::LockRect","direct3d9.idirect3dcubetexture9__lockrect"]
old-location: direct3d9\idirect3dcubetexture9__lockrect.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dcubetexture9__lockrect.htm
ms.date: 08/11/2022
ms.keywords: 1f5618d3-63b7-c0fc-9b6e-44b99c39650c, IDirect3DCubeTexture9 interface [Direct3D 9],LockRect method, IDirect3DCubeTexture9.LockRect, IDirect3DCubeTexture9::LockRect, LockRect, LockRect method [Direct3D 9], LockRect method [Direct3D 9],IDirect3DCubeTexture9 interface, d3d9helper/IDirect3DCubeTexture9::LockRect, direct3d9.idirect3dcubetexture9__lockrect
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
 - IDirect3DCubeTexture9::LockRect
 - d3d9helper/IDirect3DCubeTexture9::LockRect
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
 - IDirect3DCubeTexture9.LockRect
---

# IDirect3DCubeTexture9::LockRect


## -description

Locks a rectangle on a cube texture resource.

## -parameters

### -param FaceType [in]

Type: <b><a href="/windows/desktop/direct3d9/d3dcubemap-faces">D3DCUBEMAP_FACES</a></b>

Member of the <a href="/windows/desktop/direct3d9/d3dcubemap-faces">D3DCUBEMAP_FACES</a> enumerated type, identifying a cube map face.

### -param Level [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Specifies a level of a mipmapped cube texture.

### -param pLockedRect [out]

Type: <b><a href="/windows/desktop/direct3d9/d3dlocked-rect">D3DLOCKED_RECT</a>*</b>

Pointer to a <a href="/windows/desktop/direct3d9/d3dlocked-rect">D3DLOCKED_RECT</a> structure, describing the region to lock.

### -param pRect [in]

Type: <b>const <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

Pointer to a rectangle to lock. Specified by a pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure. Specifying <b>NULL</b> for this parameter expands the dirty region to cover the entire cube texture.

### -param Flags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Combination of zero or more locking flags that describe the type of lock to perform. For this method, the valid flags are: 



<ul>
<li>D3DLOCK_DISCARD</li>
<li>D3DLOCK_NO_DIRTY_UPDATE</li>
<li>D3DLOCK_NOSYSLOCK</li>
<li>D3DLOCK_READONLY</li>
</ul>
You may not specify a subrect when using D3DLOCK_DISCARD. For a description of the flags, see <a href="/windows/desktop/direct3d9/d3dlock">D3DLOCK</a>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. D3DERR_INVALIDCALL is returned if one or more of the arguments is invalid.

## -remarks

For performance reasons, dirty regions are only recorded for level zero of a texture. Dirty regions are automatically recorded when <b>IDirect3DCubeTexture9::LockRect</b> is called without D3DLOCK_NO_DIRTY_UPDATE or D3DLOCK_READONLY. See <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatetexture">IDirect3DDevice9::UpdateTexture</a> for more information.

Cube textures created with D3DPOOL_DEFAULT are not lockable. Cube textures created in video memory are lockable when created with <a href="/windows/desktop/direct3d9/d3dusage">USAGE_DYNAMIC</a>.

The only lockable format for a depth-stencil texture is <a href="/windows/desktop/direct3d9/d3dformat">D3DFMT_D16_LOCKABLE</a>.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9">IDirect3DCubeTexture9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3dcubetexture9-adddirtyrect">IDirect3DCubeTexture9::AddDirtyRect</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3dcubetexture9-getleveldesc">IDirect3DCubeTexture9::GetLevelDesc</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3dcubetexture9-unlockrect">IDirect3DCubeTexture9::UnlockRect</a>
