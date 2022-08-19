---
UID: NF:d3d9helper.IDirect3DTexture9.LockRect
title: IDirect3DTexture9::LockRect (d3d9helper.h)
description: The IDirect3DTexture9::LockRect method (d3d9.h) locks a rectangle on a texture resource. 
helpviewer_keywords: ["IDirect3DTexture9 interface [Direct3D 9]","LockRect method","IDirect3DTexture9.LockRect","IDirect3DTexture9::LockRect","LockRect","LockRect method [Direct3D 9]","LockRect method [Direct3D 9]","IDirect3DTexture9 interface","d0e2d5f7-5658-91b3-8546-73a643bf1df0","d3d9helper/IDirect3DTexture9::LockRect","direct3d9.idirect3dtexture9__lockrect"]
old-location: direct3d9\idirect3dtexture9__lockrect.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dtexture9__lockrect.htm
ms.date: 08/12/2022
ms.keywords: IDirect3DTexture9 interface [Direct3D 9],LockRect method, IDirect3DTexture9.LockRect, IDirect3DTexture9::LockRect, LockRect, LockRect method [Direct3D 9], LockRect method [Direct3D 9],IDirect3DTexture9 interface, d0e2d5f7-5658-91b3-8546-73a643bf1df0, d3d9helper/IDirect3DTexture9::LockRect, direct3d9.idirect3dtexture9__lockrect
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
 - IDirect3DTexture9::LockRect
 - d3d9helper/IDirect3DTexture9::LockRect
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
 - IDirect3DTexture9.LockRect
---

# IDirect3DTexture9::LockRect


## -description

Locks a rectangle on a texture resource.

## -parameters

### -param Level [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Specifies the level of the texture resource to lock.

### -param pLockedRect [out]

Type: <b><a href="/windows/desktop/direct3d9/d3dlocked-rect">D3DLOCKED_RECT</a>*</b>

Pointer to a <a href="/windows/desktop/direct3d9/d3dlocked-rect">D3DLOCKED_RECT</a> structure, describing the locked region.

### -param pRect [in]

Type: <b>const <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

Pointer to a rectangle to lock. Specified by a pointer to a RECT structure. Specifying <b>NULL</b> for this parameter expands the dirty region to cover the entire texture.

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

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.

## -remarks

Textures created with D3DPOOL_DEFAULT are not lockable. Textures created in video memory are lockable when created with <a href="/windows/desktop/direct3d9/d3dusage">USAGE_DYNAMIC</a>.

For performance reasons, dirty regions are recorded only for level zero of a texture. Dirty regions are automatically recorded when <b>IDirect3DTexture9::LockRect</b> is called without <a href="/windows/desktop/direct3d9/d3dlock">D3DLOCK_NO_DIRTY_UPDATE</a>    or D3DLOCK_READONLY. See <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatetexture">IDirect3DDevice9::UpdateTexture</a> for more information.

The only lockable format for a depth-stencil texture is <a href="/windows/desktop/direct3d9/d3dlock">D3DLOCK_D16_LOCKABLE</a>.

Video memory textures cannot be locked, but must be modified by calling <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatesurface">IDirect3DDevice9::UpdateSurface</a> or <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatetexture">IDirect3DDevice9::UpdateTexture</a>. There are exceptions for some proprietary driver pixel formats that Direct3D 9 does not recognize. These can be locked.

This method cannot retrieve data from a texture resource created with <a href="/windows/desktop/direct3d9/d3dusage">D3DUSAGE_RENDERTARGET</a> because such a texture must be assigned to D3DPOOL_DEFAULT memory and is therefore not lockable. In this case, use instead <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getrendertargetdata">IDirect3DDevice9::GetRenderTargetData</a> to copy texture data from device memory to system memory.

## -see-also

<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getrendertargetdata">IDirect3DDevice9::GetRenderTargetData</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatetexture">IDirect3DDevice9::UpdateTexture</a>



<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dtexture9">IDirect3DTexture9</a>



<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-unlockrect">IDirect3DTexture9::UnlockRect</a>
