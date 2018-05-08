---
UID: NF:d3d9helper.IDirect3D9.CreateDevice
title: IDirect3D9::CreateDevice
author: windows-driver-content
description: Creates a device to represent the display adapter.
old-location: direct3d9\idirect3d9__createdevice.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3d9__createdevice.htm
ms.author: windowsdriverdev
ms.date: 4/10/2018
ms.keywords: CreateDevice, CreateDevice method [Direct3D 9], CreateDevice method [Direct3D 9],IDirect3D9 interface, IDirect3D9 interface [Direct3D 9],CreateDevice method, IDirect3D9.CreateDevice, IDirect3D9::CreateDevice, d3d9helper/IDirect3D9::CreateDevice, direct3d9.idirect3d9__createdevice, f1a706e0-42fb-ed6e-c0c8-07fa6aef658a
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
req.typenames: D3DVSHADERCAPS2_0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D9.lib
-	D3D9.dll
api_name:
-	IDirect3D9.CreateDevice
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3D9::CreateDevice


## -description


Creates a device to represent the display adapter.


## -parameters




### -param Adapter [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Ordinal number that denotes the display adapter. <a href="https://msdn.microsoft.com/76f91917-394a-4588-9c83-c35bddb36b8e">D3DADAPTER_DEFAULT</a> is always the primary display adapter. 


### -param DeviceType [in]

Type: <b><a href="https://msdn.microsoft.com/2bcdc476-7c42-4152-b107-58366faf2abd">D3DDEVTYPE</a></b>

Member of the <a href="https://msdn.microsoft.com/2bcdc476-7c42-4152-b107-58366faf2abd">D3DDEVTYPE</a> enumerated type that denotes the desired device type. If the desired device type is not available, the method will fail. 


### -param hFocusWindow [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

The focus window alerts Direct3D when an application switches from foreground mode to background mode. See Remarks. 	
    


<ul>
<li>For full-screen mode, the window specified must be a top-level window.</li>
<li>For windowed mode, this parameter may be <b>NULL</b> only if the hDeviceWindow member of <i>pPresentationParameters</i> is set to a valid, non-<b>NULL</b> value.</li>
</ul>

### -param BehaviorFlags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Combination of one or more options that control device creation. For more information, see <a href="https://msdn.microsoft.com/91387a2d-3927-4285-a09b-9ce247e6bfdd">D3DCREATE</a>.


### -param pPresentationParameters [in, out]

Type: <b><a href="https://msdn.microsoft.com/d677aeb7-a188-4ddc-b8c9-48e13676e9c8">D3DPRESENT_PARAMETERS</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/d677aeb7-a188-4ddc-b8c9-48e13676e9c8">D3DPRESENT_PARAMETERS</a> structure, describing the presentation parameters for the device to be created. If BehaviorFlags specifies <a href="https://msdn.microsoft.com/91387a2d-3927-4285-a09b-9ce247e6bfdd">D3DCREATE_ADAPTERGROUP_DEVICE</a>, pPresentationParameters is an array. Regardless of the number of heads that exist, only one depth/stencil surface is automatically created.

For Windows 2000 and Windows XP, the full-screen device display refresh rate is set in the following order: 

<ol>
<li>User-specified nonzero ForcedRefreshRate registry key, if supported by the device.</li>
<li>Application-specified nonzero refresh rate value in the presentation parameter.</li>
<li>Refresh rate of the latest desktop, if supported by the device.</li>
<li>75 hertz if supported by the device.</li>
<li>60 hertz if supported by the device.</li>
<li>Device default.</li>
</ol>
An unsupported refresh rate will default to the closest supported refresh rate below it.  For example, if the application specifies 63 hertz, 60 hertz will be used. There are no supported refresh rates below 57 hertz.

pPresentationParameters is both an input and an output parameter. Calling this method may change several members including:

<ul>
<li>If BackBufferCount, BackBufferWidth, and BackBufferHeight  are 0 before the method is called, they will be changed when the method returns.</li>
<li>If BackBufferFormat equals <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFMT_UNKNOWN</a> before the method is called, it will be changed when the method returns.</li>
</ul>

### -param ppReturnedDeviceInterface [out, retval]

Type: <b><a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>**</b>

Address of a pointer to the returned <a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a> interface, which represents the created device. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_DEVICELOST, D3DERR_INVALIDCALL, D3DERR_NOTAVAILABLE, D3DERR_OUTOFVIDEOMEMORY.




## -remarks



This method returns a fully working device interface, set to the required display mode (or windowed), and allocated with the appropriate back buffers. To begin rendering, the application needs only to create and set a depth buffer (assuming EnableAutoDepthStencil is <b>FALSE</b> in <a href="https://msdn.microsoft.com/d677aeb7-a188-4ddc-b8c9-48e13676e9c8">D3DPRESENT_PARAMETERS</a>).

When you create a Direct3D device, you supply two different window parameters: a focus window (hFocusWindow) and a device window (the hDeviceWindow in <a href="https://msdn.microsoft.com/d677aeb7-a188-4ddc-b8c9-48e13676e9c8">D3DPRESENT_PARAMETERS</a>). The purpose of each window is:

<ul>
<li>The focus window alerts Direct3D when an application switches from foreground mode to background mode (via Alt-Tab, a mouse click, or some other method). A single focus window is shared by each device created by an application.</li>
<li>The device window determines the location and size of the back buffer on screen. This is used by Direct3D when the back buffer contents are copied to the front buffer during <a href="https://msdn.microsoft.com/47e67956-7ab4-4e05-bf05-685bdc094cf2">Present</a>.</li>
</ul>
This method should not be run during the handling of WM_CREATE. An application should never pass a window handle to Direct3D while handling WM_CREATE. 
    
    Any call to create, release, or reset the device must be done using the same thread as the window procedure of the focus window.

Note that D3DCREATE_HARDWARE_VERTEXPROCESSING, D3DCREATE_MIXED_VERTEXPROCESSING, and D3DCREATE_SOFTWARE_VERTEXPROCESSING are mutually exclusive flags, and at least one of these vertex processing flags must be specified when calling this method.

Back buffers created as part of the device are only lockable if D3DPRESENTFLAG_LOCKABLE_BACKBUFFER is specified in the presentation parameters. (Multisampled back buffers and depth surfaces are never lockable.)

The methods <a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>, <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>, and <a href="https://msdn.microsoft.com/da2ac8dd-0df8-4661-995f-9c3e6ccb62d2">TestCooperativeLevel</a> must be called from the same thread that used this method to create a device.

D3DFMT_UNKNOWN can be specified for the windowed mode back buffer format when calling <b>CreateDevice</b>, <a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>, and <a href="https://msdn.microsoft.com/d41b36f6-8481-47f8-bd38-8f51bc9ff9b8">CreateAdditionalSwapChain</a>. This means the application does not have to query the current desktop format before calling <b>CreateDevice</b> for windowed mode. For full-screen mode, the back buffer format must be specified.

If you attempt to create a device on a 0x0 sized window, <b>CreateDevice</b> will fail.




## -see-also




<a href="https://msdn.microsoft.com/7db5ef2b-6894-4113-b726-8b238bb4fb2f">D3DDEVICE_CREATION_PARAMETERS</a>



<a href="https://msdn.microsoft.com/33573d84-8bae-4cac-80d1-fe7387d9d7eb">Direct3DCreate9</a>



<a href="https://msdn.microsoft.com/af321e4f-aaff-4285-bdac-9aab5c1dc5d8">IDirect3D9</a>



<a href="https://msdn.microsoft.com/f741cdb4-2eb6-42e9-81ea-a8c677e07582">Multihead (Direct3D 9)</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>
 

 

