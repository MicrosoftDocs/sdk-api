---
UID: NF:d3d9helper.IDirect3DSurface9.GetDC
title: IDirect3DSurface9::GetDC
author: windows-sdk-content
description: Retrieves a device context.
old-location: direct3d9\idirect3dsurface9__getdc.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dsurface9__getdc.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: 945f6e77-19f2-e9bf-18a4-09747a9990f3, GetDC, GetDC method [Direct3D 9], GetDC method [Direct3D 9],IDirect3DSurface9 interface, IDirect3DSurface9 interface [Direct3D 9],GetDC method, IDirect3DSurface9.GetDC, IDirect3DSurface9::GetDC, d3d9helper/IDirect3DSurface9::GetDC, direct3d9.idirect3dsurface9__getdc
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDirect3DSurface9.GetDC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DSurface9::GetDC


## -description


Retrieves a device context.


## -parameters




### -param phdc [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a>*</b>

Pointer to the device context for the surface.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. D3DERR_INVALIDCALL is returned if the argument is invalid.




## -remarks



The following restrictions apply.

<ul>
<li><b>IDirect3DSurface9::GetDC</b> is valid on the following formats only: D3DFMT_R5G6B5, D3DFMT_X1R5G5B5, D3DFMT_R8G8B8, and D3DFMT_X8R8G8B8. Formats that contain Alpha are not supported because the GDI implementations don't have a well-defined behavior on the alpha channel. For more information about formats, see <a href="https://msdn.microsoft.com/en-us/library/Bb172558(v=VS.85).aspx">D3DFORMAT</a>.</li>
<li>Only one device context per surface can be returned at a time.</li>
<li><b>IDirect3DSurface9::GetDC</b> will fail if the surface is already locked. If the surface is a member of a mipmap or cubemap, <b>IDirect3DSurface9::GetDC</b> fails if any other mipmap or cubemap member is locked.</li>
<li><b>IDirect3DSurface9::GetDC</b> fails on render targets unless they were created lockable (or, in the case of back buffers, with the D3DPRESENTFLAG_LOCKABLE_BACKBUFFER flag).</li>
<li>For surfaces not created with <a href="https://msdn.microsoft.com/en-us/library/Bb174358(v=VS.85).aspx">IDirect3DDevice9::CreateOffscreenPlainSurface</a>, <b>IDirect3DSurface9::GetDC</b> will fail on default pool (D3DPOOL_DEFAULT) surfaces unless they are dynamic (D3DUSAGE_DYNAMIC) or are lockable render targets.</li>
<li><b>IDirect3DSurface9::GetDC</b> will fail on D3DPOOL_SCRATCH surfaces.</li>
</ul>
When a device context is outstanding on a surface, the application may not call these methods:

<table>
<tr>
<td>IDirect3DCubeTexture9</td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Bb174334(v=VS.85).aspx">IDirect3DCubeTexture9::LockRect</a>
</td>
</tr>
<tr>
<td>IDirect3DDevice9</td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Bb174353(v=VS.85).aspx">IDirect3DDevice9::ColorFill</a>
</td>
</tr>
<tr>
<td></td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Bb174471(v=VS.85).aspx">IDirect3DDevice9::StretchRect</a>
</td>
</tr>
<tr>
<td></td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Bb205857(v=VS.85).aspx">IDirect3DDevice9::UpdateSurface</a>
</td>
</tr>
<tr>
<td></td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Bb205858(v=VS.85).aspx">IDirect3DDevice9::UpdateTexture</a>
</td>
</tr>
<tr>
<td>IDirect3DSurface9</td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Bb205896(v=VS.85).aspx">IDirect3DSurface9::LockRect</a>
</td>
</tr>
<tr>
<td>IDirect3DSwapChain9</td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Bb205908(v=VS.85).aspx">IDirect3DSwapChain9::Present</a> *</td>
</tr>
<tr>
<td>IDirect3DTexture9</td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Bb205913(v=VS.85).aspx">IDirect3DTexture9::LockRect</a>
</td>
</tr>
</table>
 

* (on a swap chain that contains the surface)

<b>IDirect3DSurface9::GetDC</b> causes an implicit lock; do not retain the device context for later use. Call <a href="https://msdn.microsoft.com/en-us/library/Bb205897(v=VS.85).aspx">IDirect3DSurface9::ReleaseDC</a> to release it.	

It is valid to call <b>IDirect3DSurface9::GetDC</b>/<a href="https://msdn.microsoft.com/en-us/library/Bb205897(v=VS.85).aspx">IDirect3DSurface9::ReleaseDC</a> on levels of a mipmap or cubemap, however, these calls will be slow to all miplevels except the topmost level, and GDI operations to these miplevels will not be accelerated.

The hdc provides access to Win32 and GDI functionality.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb172584(v=VS.85).aspx">D3DPOOL</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb172588(v=VS.85).aspx">D3DPRESENT_PARAMETERS</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb172625(v=VS.85).aspx">D3DUSAGE</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb205892(v=VS.85).aspx">IDirect3DSurface9</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb205897(v=VS.85).aspx">IDirect3DSurface9::ReleaseDC</a>
 

 

