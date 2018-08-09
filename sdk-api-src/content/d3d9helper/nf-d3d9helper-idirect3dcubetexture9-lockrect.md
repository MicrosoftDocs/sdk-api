---
UID: NF:d3d9helper.IDirect3DCubeTexture9.LockRect
title: IDirect3DCubeTexture9::LockRect
author: windows-sdk-content
description: Locks a rectangle on a cube texture resource.
old-location: direct3d9\idirect3dcubetexture9__lockrect.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dcubetexture9__lockrect.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 1f5618d3-63b7-c0fc-9b6e-44b99c39650c, IDirect3DCubeTexture9 interface [Direct3D 9],LockRect method, IDirect3DCubeTexture9.LockRect, IDirect3DCubeTexture9::LockRect, LockRect, LockRect method [Direct3D 9], LockRect method [Direct3D 9],IDirect3DCubeTexture9 interface, d3d9helper/IDirect3DCubeTexture9::LockRect, direct3d9.idirect3dcubetexture9__lockrect
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: D3DVSHADERCAPS2_0
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
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DCubeTexture9::LockRect


## -description


Locks a rectangle on a cube texture resource.


## -parameters




### -param FaceType [in]

Type: <b><a href="https://msdn.microsoft.com/6d18b410-6f22-4202-86ae-6b3ef85e6f69">D3DCUBEMAP_FACES</a></b>

Member of the <a href="https://msdn.microsoft.com/6d18b410-6f22-4202-86ae-6b3ef85e6f69">D3DCUBEMAP_FACES</a> enumerated type, identifying a cube map face. 


### -param Level [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Specifies a level of a mipmapped cube texture. 


### -param pLockedRect [out]

Type: <b><a href="https://msdn.microsoft.com/ee5d2ea6-bf98-4b09-bc67-b808ffcb23c6">D3DLOCKED_RECT</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/ee5d2ea6-bf98-4b09-bc67-b808ffcb23c6">D3DLOCKED_RECT</a> structure, describing the region to lock. 


### -param pRect [in]

Type: <b>const <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>*</b>

Pointer to a rectangle to lock. Specified by a pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure. Specifying <b>NULL</b> for this parameter expands the dirty region to cover the entire cube texture.


### -param Flags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Combination of zero or more locking flags that describe the type of lock to perform. For this method, the valid flags are: 



<ul>
<li>D3DLOCK_DISCARD</li>
<li>D3DLOCK_NO_DIRTY_UPDATE</li>
<li>D3DLOCK_NOSYSLOCK</li>
<li>D3DLOCK_READONLY</li>
</ul>
You may not specify a subrect when using D3DLOCK_DISCARD. For a description of the flags, see <a href="https://msdn.microsoft.com/46a611bd-a1ec-4967-b68d-72661d1b5cad">D3DLOCK</a>.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. D3DERR_INVALIDCALL is returned if one or more of the arguments is invalid.




## -remarks



For performance reasons, dirty regions are only recorded for level zero of a texture. Dirty regions are automatically recorded when <b>IDirect3DCubeTexture9::LockRect</b> is called without D3DLOCK_NO_DIRTY_UPDATE or D3DLOCK_READONLY. See <a href="https://msdn.microsoft.com/79be31d9-0dd2-416c-b58c-9b3b7777c65c">IDirect3DDevice9::UpdateTexture</a> for more information.

Cube textures created with D3DPOOL_DEFAULT are not lockable. Cube textures created in video memory are lockable when created with <a href="https://msdn.microsoft.com/c8823c39-8f17-441c-a42b-de3d7ec02f75">USAGE_DYNAMIC</a>.

The only lockable format for a depth-stencil texture is <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFMT_D16_LOCKABLE</a>.




## -see-also




<a href="https://msdn.microsoft.com/59e400ae-d2ec-425c-9adf-49cb5a24c808">IDirect3DCubeTexture9</a>



<a href="https://msdn.microsoft.com/377536bd-c55c-4ec8-a07c-5addd8e84c3a">IDirect3DCubeTexture9::AddDirtyRect</a>



<a href="https://msdn.microsoft.com/0b3efd79-cd69-4eea-af3a-4aa4d3f79e97">IDirect3DCubeTexture9::GetLevelDesc</a>



<a href="https://msdn.microsoft.com/3e444bdc-c555-465d-84a8-96aef32d3e77">IDirect3DCubeTexture9::UnlockRect</a>
 

 

