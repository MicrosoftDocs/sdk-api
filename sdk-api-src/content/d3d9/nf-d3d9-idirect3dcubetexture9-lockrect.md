---
UID: NF:d3d9.IDirect3DCubeTexture9.LockRect
title: IDirect3DCubeTexture9::LockRect (d3d9.h)
author: windows-sdk-content
description: Locks a rectangle on a cube texture resource.
old-location: direct3d9\idirect3dcubetexture9__lockrect.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dcubetexture9__lockrect.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 1f5618d3-63b7-c0fc-9b6e-44b99c39650c, IDirect3DCubeTexture9 interface [Direct3D 9],LockRect method, IDirect3DCubeTexture9.LockRect, IDirect3DCubeTexture9::LockRect, LockRect, LockRect method [Direct3D 9], LockRect method [Direct3D 9],IDirect3DCubeTexture9 interface, d3d9helper/IDirect3DCubeTexture9::LockRect, direct3d9.idirect3dcubetexture9__lockrect
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirect3DCubeTexture9::LockRect


## -description


Locks a rectangle on a cube texture resource.


## -parameters




### -param FaceType [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172528(v=VS.85).aspx">D3DCUBEMAP_FACES</a></b>

Member of the <a href="https://msdn.microsoft.com/en-us/library/Bb172528(v=VS.85).aspx">D3DCUBEMAP_FACES</a> enumerated type, identifying a cube map face. 


### -param Level [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Specifies a level of a mipmapped cube texture. 


### -param pLockedRect [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172570(v=VS.85).aspx">D3DLOCKED_RECT</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/Bb172570(v=VS.85).aspx">D3DLOCKED_RECT</a> structure, describing the region to lock. 


### -param pRect [in]

Type: <b>const <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>*</b>

Pointer to a rectangle to lock. Specified by a pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure. Specifying <b>NULL</b> for this parameter expands the dirty region to cover the entire cube texture.


### -param Flags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Combination of zero or more locking flags that describe the type of lock to perform. For this method, the valid flags are: 



<ul>
<li>D3DLOCK_DISCARD</li>
<li>D3DLOCK_NO_DIRTY_UPDATE</li>
<li>D3DLOCK_NOSYSLOCK</li>
<li>D3DLOCK_READONLY</li>
</ul>
You may not specify a subrect when using D3DLOCK_DISCARD. For a description of the flags, see <a href="https://msdn.microsoft.com/en-us/library/Bb172568(v=VS.85).aspx">D3DLOCK</a>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. D3DERR_INVALIDCALL is returned if one or more of the arguments is invalid.




## -remarks



For performance reasons, dirty regions are only recorded for level zero of a texture. Dirty regions are automatically recorded when <b>IDirect3DCubeTexture9::LockRect</b> is called without D3DLOCK_NO_DIRTY_UPDATE or D3DLOCK_READONLY. See <a href="https://msdn.microsoft.com/en-us/library/Bb205858(v=VS.85).aspx">IDirect3DDevice9::UpdateTexture</a> for more information.

Cube textures created with D3DPOOL_DEFAULT are not lockable. Cube textures created in video memory are lockable when created with <a href="https://msdn.microsoft.com/en-us/library/Bb172625(v=VS.85).aspx">USAGE_DYNAMIC</a>.

The only lockable format for a depth-stencil texture is <a href="https://msdn.microsoft.com/en-us/library/Bb172558(v=VS.85).aspx">D3DFMT_D16_LOCKABLE</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174329(v=VS.85).aspx">IDirect3DCubeTexture9</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174330(v=VS.85).aspx">IDirect3DCubeTexture9::AddDirtyRect</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174332(v=VS.85).aspx">IDirect3DCubeTexture9::GetLevelDesc</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174335(v=VS.85).aspx">IDirect3DCubeTexture9::UnlockRect</a>
 

 

