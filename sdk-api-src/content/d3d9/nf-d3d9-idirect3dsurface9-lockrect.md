---
UID: NF:d3d9.IDirect3DSurface9.LockRect
title: IDirect3DSurface9::LockRect
author: windows-sdk-content
description: Locks a rectangle on a surface.
old-location: direct3d9\idirect3dsurface9__lockrect.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dsurface9__lockrect.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: 95e6910d-b701-2649-b38f-7c2f4fe99c47, IDirect3DSurface9 interface [Direct3D 9],LockRect method, IDirect3DSurface9.LockRect, IDirect3DSurface9::LockRect, LockRect, LockRect method [Direct3D 9], LockRect method [Direct3D 9],IDirect3DSurface9 interface, d3d9helper/IDirect3DSurface9::LockRect, direct3d9.idirect3dsurface9__lockrect
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDirect3DSurface9.LockRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DSurface9::LockRect


## -description


Locks a rectangle on a surface.


## -parameters




### -param pLockedRect [out]

Type: <b><a href="https://msdn.microsoft.com/ee5d2ea6-bf98-4b09-bc67-b808ffcb23c6">D3DLOCKED_RECT</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/ee5d2ea6-bf98-4b09-bc67-b808ffcb23c6">D3DLOCKED_RECT</a> structure that describes the locked region. 


### -param pRect [in]

Type: <b>const <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>*</b>

Pointer to a rectangle to lock. Specified by a pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure. Specifying <b>NULL</b> for this parameter expands the dirty region to cover the entire surface. 


### -param Flags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Combination of zero or more locking flags that describe the type of lock to perform. For this method, the valid flags are: 
    


<ul>
<li>D3DLOCK_DISCARD</li>
<li>D3DLOCK_DONOTWAIT</li>
<li>D3DLOCK_NO_DIRTY_UPDATE</li>
<li>D3DLOCK_NOSYSLOCK</li>
<li>D3DLOCK_READONLY</li>
</ul>
You may not specify a subrect when using D3DLOCK_DISCARD. For a description of the flags, see <a href="https://msdn.microsoft.com/46a611bd-a1ec-4967-b68d-72661d1b5cad">D3DLOCK</a>.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK.

If the method fails, the return value can be D3DERR_INVALIDCALL or D3DERR_WASSTILLDRAWING.




## -remarks



If the <a href="https://msdn.microsoft.com/46a611bd-a1ec-4967-b68d-72661d1b5cad">D3DLOCK_DONOTWAIT</a> flag is specified and the driver cannot lock the surface immediately, <b>IDirect3DSurface9::LockRect</b> will return D3DERR_WASSTILLDRAWING so that an application can use the CPU cycles while waiting for the driver to lock the surface.

The only lockable format for a depth-stencil surface is D3DFMT_D16_LOCKABLE. See <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a>.

For performance reasons, dirty regions are recorded only for level zero of a texture. Dirty regions are automatically recorded when <b>IDirect3DSurface9::LockRect</b> is called without <a href="https://msdn.microsoft.com/46a611bd-a1ec-4967-b68d-72661d1b5cad">D3DLOCK_NO_DIRTY_UPDATE</a>    or D3DLOCK_READONLY. See <a href="https://msdn.microsoft.com/79be31d9-0dd2-416c-b58c-9b3b7777c65c">IDirect3DDevice9::UpdateTexture</a> for more information.

A multisample back buffer cannot be locked.

This method cannot retrieve data from a surface that is is contained by a texture resource created with <a href="https://msdn.microsoft.com/c8823c39-8f17-441c-a42b-de3d7ec02f75">D3DUSAGE_RENDERTARGET</a> because such a texture must be assigned to D3DPOOL_DEFAULT memory and is therefore not lockable. In this case, use instead <a href="https://msdn.microsoft.com/9fc6121c-3da8-49d8-9bd6-c8654ce90100">IDirect3DDevice9::GetRenderTargetData</a> to copy texture data from device memory to system memory.




## -see-also




<a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a>



<a href="https://msdn.microsoft.com/7dc45972-fc17-4a60-9e4a-1d28a379e08f">IDirect3DSurface9::UnlockRect</a>
 

 

