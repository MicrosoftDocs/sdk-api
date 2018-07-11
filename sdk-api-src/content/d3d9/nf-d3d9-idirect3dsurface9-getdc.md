---
UID: NF:d3d9.IDirect3DSurface9.GetDC
title: IDirect3DSurface9::GetDC
author: windows-sdk-content
description: Retrieves a device context.
old-location: direct3d9\idirect3dsurface9__getdc.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dsurface9__getdc.htm
ms.author: windowssdkdev
ms.date: 04/11/2018
ms.keywords: 945f6e77-19f2-e9bf-18a4-09747a9990f3, GetDC, GetDC method [Direct3D 9], GetDC method [Direct3D 9],IDirect3DSurface9 interface, IDirect3DSurface9 interface [Direct3D 9],GetDC method, IDirect3DSurface9.GetDC, IDirect3DSurface9::GetDC, d3d9helper/IDirect3DSurface9::GetDC, direct3d9.idirect3dsurface9__getdc
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D12_SIGNATURE_PARAMETER_DESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DSurface9.GetDC
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DSurface9::GetDC


## -description


Retrieves a device context.


## -parameters




### -param phdc [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a>*</b>

Pointer to the device context for the surface.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. D3DERR_INVALIDCALL is returned if the argument is invalid.




## -remarks



The following restrictions apply.

<ul>
<li><b>IDirect3DSurface9::GetDC</b> is valid on the following formats only: D3DFMT_R5G6B5, D3DFMT_X1R5G5B5, D3DFMT_R8G8B8, and D3DFMT_X8R8G8B8. Formats that contain Alpha are not supported because the GDI implementations don't have a well-defined behavior on the alpha channel. For more information about formats, see <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a>.</li>
<li>Only one device context per surface can be returned at a time.</li>
<li><b>IDirect3DSurface9::GetDC</b> will fail if the surface is already locked. If the surface is a member of a mipmap or cubemap, <b>IDirect3DSurface9::GetDC</b> fails if any other mipmap or cubemap member is locked.</li>
<li><b>IDirect3DSurface9::GetDC</b> fails on render targets unless they were created lockable (or, in the case of back buffers, with the D3DPRESENTFLAG_LOCKABLE_BACKBUFFER flag).</li>
<li>For surfaces not created with <a href="https://msdn.microsoft.com/9502aa34-afde-4547-a5da-224f29719c07">IDirect3DDevice9::CreateOffscreenPlainSurface</a>, <b>IDirect3DSurface9::GetDC</b> will fail on default pool (D3DPOOL_DEFAULT) surfaces unless they are dynamic (D3DUSAGE_DYNAMIC) or are lockable render targets.</li>
<li><b>IDirect3DSurface9::GetDC</b> will fail on D3DPOOL_SCRATCH surfaces.</li>
</ul>
When a device context is outstanding on a surface, the application may not call these methods:

<table>
<tr>
<td>IDirect3DCubeTexture9</td>
<td>
<a href="https://msdn.microsoft.com/724317a3-1fc7-499d-94b7-759731337a00">IDirect3DCubeTexture9::LockRect</a>
</td>
</tr>
<tr>
<td>IDirect3DDevice9</td>
<td>
<a href="https://msdn.microsoft.com/de8c1f15-cb82-4c20-86e0-78b730dae55d">IDirect3DDevice9::ColorFill</a>
</td>
</tr>
<tr>
<td></td>
<td>
<a href="https://msdn.microsoft.com/1ad6d48f-8420-461a-96b5-e730ac06c393">IDirect3DDevice9::StretchRect</a>
</td>
</tr>
<tr>
<td></td>
<td>
<a href="https://msdn.microsoft.com/303a4224-9c5d-4fc6-a7c5-168f18166e3c">IDirect3DDevice9::UpdateSurface</a>
</td>
</tr>
<tr>
<td></td>
<td>
<a href="https://msdn.microsoft.com/79be31d9-0dd2-416c-b58c-9b3b7777c65c">IDirect3DDevice9::UpdateTexture</a>
</td>
</tr>
<tr>
<td>IDirect3DSurface9</td>
<td>
<a href="https://msdn.microsoft.com/01f5a1a1-e18f-42c9-9654-34e482f48df8">IDirect3DSurface9::LockRect</a>
</td>
</tr>
<tr>
<td>IDirect3DSwapChain9</td>
<td>
<a href="https://msdn.microsoft.com/ac90aee6-dd66-46d8-a628-4bf8bff087b4">IDirect3DSwapChain9::Present</a> *</td>
</tr>
<tr>
<td>IDirect3DTexture9</td>
<td>
<a href="https://msdn.microsoft.com/b1c3905a-a253-4e3d-b0b2-99c839a5e6d9">IDirect3DTexture9::LockRect</a>
</td>
</tr>
</table>
 

* (on a swap chain that contains the surface)

<b>IDirect3DSurface9::GetDC</b> causes an implicit lock; do not retain the device context for later use. Call <a href="https://msdn.microsoft.com/90a21163-65c2-4409-a18f-5c9a377e9d66">IDirect3DSurface9::ReleaseDC</a> to release it.	

It is valid to call <b>IDirect3DSurface9::GetDC</b>/<a href="https://msdn.microsoft.com/90a21163-65c2-4409-a18f-5c9a377e9d66">IDirect3DSurface9::ReleaseDC</a> on levels of a mipmap or cubemap, however, these calls will be slow to all miplevels except the topmost level, and GDI operations to these miplevels will not be accelerated.

The hdc provides access to Win32 and GDI functionality.




## -see-also




<a href="https://msdn.microsoft.com/29720b5f-16d7-4bd9-a7bd-e4dbfb00070b">D3DPOOL</a>



<a href="https://msdn.microsoft.com/d677aeb7-a188-4ddc-b8c9-48e13676e9c8">D3DPRESENT_PARAMETERS</a>



<a href="https://msdn.microsoft.com/c8823c39-8f17-441c-a42b-de3d7ec02f75">D3DUSAGE</a>



<a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a>



<a href="https://msdn.microsoft.com/90a21163-65c2-4409-a18f-5c9a377e9d66">IDirect3DSurface9::ReleaseDC</a>
 

 

