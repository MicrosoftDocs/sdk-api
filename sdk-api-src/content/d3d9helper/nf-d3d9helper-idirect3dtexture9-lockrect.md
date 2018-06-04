---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IDirect3DTexture9::LockRect


## -description


Locks a rectangle on a texture resource.


## -parameters




### -param Level [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Specifies the level of the texture resource to lock. 


### -param pLockedRect [out]

Type: <b><a href="https://msdn.microsoft.com/ee5d2ea6-bf98-4b09-bc67-b808ffcb23c6">D3DLOCKED_RECT</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/ee5d2ea6-bf98-4b09-bc67-b808ffcb23c6">D3DLOCKED_RECT</a> structure, describing the locked region. 


### -param pRect [in]

Type: <b>const <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>*</b>

Pointer to a rectangle to lock. Specified by a pointer to a RECT structure. Specifying <b>NULL</b> for this parameter expands the dirty region to cover the entire texture. 


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

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -remarks



Textures created with D3DPOOL_DEFAULT are not lockable. Textures created in video memory are lockable when created with <a href="https://msdn.microsoft.com/c8823c39-8f17-441c-a42b-de3d7ec02f75">USAGE_DYNAMIC</a>.

For performance reasons, dirty regions are recorded only for level zero of a texture. Dirty regions are automatically recorded when <b>IDirect3DTexture9::LockRect</b> is called without <a href="https://msdn.microsoft.com/46a611bd-a1ec-4967-b68d-72661d1b5cad">D3DLOCK_NO_DIRTY_UPDATE</a>    or D3DLOCK_READONLY. See <a href="https://msdn.microsoft.com/79be31d9-0dd2-416c-b58c-9b3b7777c65c">IDirect3DDevice9::UpdateTexture</a> for more information.

The only lockable format for a depth-stencil texture is <a href="https://msdn.microsoft.com/46a611bd-a1ec-4967-b68d-72661d1b5cad">D3DLOCK_D16_LOCKABLE</a>.

Video memory textures cannot be locked, but must be modified by calling <a href="https://msdn.microsoft.com/303a4224-9c5d-4fc6-a7c5-168f18166e3c">IDirect3DDevice9::UpdateSurface</a> or <a href="https://msdn.microsoft.com/79be31d9-0dd2-416c-b58c-9b3b7777c65c">IDirect3DDevice9::UpdateTexture</a>. There are exceptions for some proprietary driver pixel formats that Direct3D 9 does not recognize. These can be locked.

This method cannot retrieve data from a texture resource created with <a href="https://msdn.microsoft.com/c8823c39-8f17-441c-a42b-de3d7ec02f75">D3DUSAGE_RENDERTARGET</a> because such a texture must be assigned to D3DPOOL_DEFAULT memory and is therefore not lockable. In this case, use instead <a href="https://msdn.microsoft.com/9fc6121c-3da8-49d8-9bd6-c8654ce90100">IDirect3DDevice9::GetRenderTargetData</a> to copy texture data from device memory to system memory.




## -see-also




<a href="https://msdn.microsoft.com/9fc6121c-3da8-49d8-9bd6-c8654ce90100">IDirect3DDevice9::GetRenderTargetData</a>



<a href="https://msdn.microsoft.com/79be31d9-0dd2-416c-b58c-9b3b7777c65c">IDirect3DDevice9::UpdateTexture</a>



<a href="https://msdn.microsoft.com/fcea1048-1d9b-409f-9b5a-cdf85c30c76e">IDirect3DTexture9</a>



<a href="https://msdn.microsoft.com/728ead50-5d2e-45a7-a91d-e2d520171d1d">IDirect3DTexture9::UnlockRect</a>
 

 

