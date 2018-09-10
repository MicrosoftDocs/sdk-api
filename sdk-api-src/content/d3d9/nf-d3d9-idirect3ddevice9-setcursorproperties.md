---
UID: NF:d3d9.IDirect3DDevice9.SetCursorProperties
title: IDirect3DDevice9::SetCursorProperties
author: windows-sdk-content
description: Sets properties for the cursor.
old-location: direct3d9\idirect3ddevice9__setcursorproperties.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setcursorproperties.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: 32bc3446-e6cd-3ae1-00fd-9614c3cf7e8d, IDirect3DDevice9 interface [Direct3D 9],SetCursorProperties method, IDirect3DDevice9.SetCursorProperties, IDirect3DDevice9::SetCursorProperties, SetCursorProperties, SetCursorProperties method [Direct3D 9], SetCursorProperties method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::SetCursorProperties, direct3d9.idirect3ddevice9__setcursorproperties
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
 - IDirect3DDevice9.SetCursorProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DDevice9::SetCursorProperties


## -description


Sets properties for the cursor.


## -parameters




### -param XHotSpot [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

X-coordinate offset (in pixels) that marks the center of the cursor. The offset is relative to the upper-left corner of the cursor. When the cursor is given a new position, the image is drawn at an offset from this new position determined by subtracting the hot spot coordinates from the position. 


### -param YHotSpot [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Y-coordinate offset (in pixels) that marks the center of the cursor. The offset is relative to the upper-left corner of the cursor. When the cursor is given a new position, the image is drawn at an offset from this new position determined by subtracting the hot spot coordinates from the position. 


### -param pCursorBitmap [in]

Type: <b><a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a> interface. This parameter must point to an 8888 ARGB surface (format D3DFMT_A8R8G8B8). The contents of this surface will be copied and potentially format-converted into an internal buffer from which the cursor is displayed. The dimensions of this surface must be less than the dimensions of the display mode, and must be a power of two in each direction, although not necessarily the same power of two. The alpha channel must be either 0.0 or 1.0. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -remarks



An operating system cursor is created and used under either of these conditions:

<ul>
<li>The hardware has set D3DCURSORCAPS_COLOR (see <a href="https://msdn.microsoft.com/b763b994-6488-40c0-9c14-e00b19e818b0">D3DCURSORCAPS</a>), and the cursor size is 32x32 (which is the cursor size in the operating system).</li>
<li>The application is running in windowed mode.</li>
</ul>
Otherwise, DirectX uses an emulated cursor. An application uses <a href="https://msdn.microsoft.com/3b6410e5-fdeb-4390-b0c6-227f0c6666c6">IDirect3DDevice9::SetCursorPosition</a> to move an emulated cursor to follow mouse movement.

It is recommended for applications to always trap WM_MOUSEMOVE events and call DXSetCursorPosition.

Direct3D cursor functions use either GDI cursor or software emulation, depending on the hardware. Users typically want to respond to a WM_SETCURSOR message. For example, they might want to write the message handler as follows:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
case WM_SETCURSOR:
// Turn off window cursor. 
SetCursor( NULL );
m_pd3dDevice-&gt;ShowCursor( TRUE );
return TRUE; // Prevent Windows from setting cursor to window class cursor.
break;
</pre>
</td>
</tr>
</table></span></div>
Or, users might want to call the <b>IDirect3DDevice9::SetCursorProperties</b> method if they want to change the cursor. 

The application can determine what hardware support is available for cursors by examining appropriate members of the <a href="https://msdn.microsoft.com/44457b7b-a1f7-4019-b971-8ec2334d3313">D3DCAPS9</a> structure. Typically, hardware supports only 32x32 cursors and, when windowed, the system might support only 32x32 cursors. In this case, <b>IDirect3DDevice9::SetCursorProperties</b> still succeeds but the cursor might be reduced to that size. The hot spot is scaled appropriately.

The cursor does not survive when the device is lost. This method must be called after the device is reset.




## -see-also




<a href="https://msdn.microsoft.com/44457b7b-a1f7-4019-b971-8ec2334d3313">D3DCAPS9</a>



<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/76d848f1-a426-489f-9207-ef708adea1be">IDirect3DDevice9::ShowCursor</a>
 

 

