---
UID: NF:d3d9.IDirect3D9.CreateDevice
title: IDirect3D9::CreateDevice (d3d9.h)
description: The IDirect3D9::CreateDevice method (d3d9.h) creates a device to represent the display adapter. 
helpviewer_keywords: ["CreateDevice","CreateDevice method [Direct3D 9]","CreateDevice method [Direct3D 9]","IDirect3D9 interface","IDirect3D9 interface [Direct3D 9]","CreateDevice method","IDirect3D9.CreateDevice","IDirect3D9::CreateDevice","d3d9helper/IDirect3D9::CreateDevice","direct3d9.idirect3d9__createdevice","f1a706e0-42fb-ed6e-c0c8-07fa6aef658a"]
old-location: direct3d9\idirect3d9__createdevice.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3d9__createdevice.htm
ms.date: 08/10/2022
ms.keywords: CreateDevice, CreateDevice method [Direct3D 9], CreateDevice method [Direct3D 9],IDirect3D9 interface, IDirect3D9 interface [Direct3D 9],CreateDevice method, IDirect3D9.CreateDevice, IDirect3D9::CreateDevice, d3d9helper/IDirect3D9::CreateDevice, direct3d9.idirect3d9__createdevice, f1a706e0-42fb-ed6e-c0c8-07fa6aef658a
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirect3D9::CreateDevice
 - d3d9/IDirect3D9::CreateDevice
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
 - IDirect3D9.CreateDevice
---

# IDirect3D9::CreateDevice


## -description

Creates a device to represent the display adapter.

## -parameters

### -param Adapter [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Ordinal number that denotes the display adapter. <a href="/windows/desktop/direct3d9/d3dadapter-default">D3DADAPTER_DEFAULT</a> is always the primary display adapter.

### -param DeviceType [in]

Type: <b><a href="/windows/desktop/direct3d9/d3ddevtype">D3DDEVTYPE</a></b>

Member of the <a href="/windows/desktop/direct3d9/d3ddevtype">D3DDEVTYPE</a> enumerated type that denotes the desired device type. If the desired device type is not available, the method will fail.

### -param hFocusWindow [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

The focus window alerts Direct3D when an application switches from foreground mode to background mode. See Remarks. 	
    


<ul>
<li>For full-screen mode, the window specified must be a top-level window.</li>
<li>For windowed mode, this parameter may be <b>NULL</b> only if the hDeviceWindow member of <i>pPresentationParameters</i> is set to a valid, non-<b>NULL</b> value.</li>
</ul>

### -param BehaviorFlags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Combination of one or more options that control device creation. For more information, see <a href="/windows/desktop/direct3d9/d3dcreate">D3DCREATE</a>.

### -param pPresentationParameters [in, out]

Type: <b><a href="/windows/desktop/direct3d9/d3dpresent-parameters">D3DPRESENT_PARAMETERS</a>*</b>

Pointer to a <a href="/windows/desktop/direct3d9/d3dpresent-parameters">D3DPRESENT_PARAMETERS</a> structure, describing the presentation parameters for the device to be created. If BehaviorFlags specifies <a href="/windows/desktop/direct3d9/d3dcreate">D3DCREATE_ADAPTERGROUP_DEVICE</a>, pPresentationParameters is an array. Regardless of the number of heads that exist, only one depth/stencil surface is automatically created.

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
<li>If BackBufferFormat equals <a href="/windows/desktop/direct3d9/d3dformat">D3DFMT_UNKNOWN</a> before the method is called, it will be changed when the method returns.</li>
</ul>

### -param ppReturnedDeviceInterface [out, retval]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>**</b>

Address of a pointer to the returned <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a> interface, which represents the created device.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_DEVICELOST, D3DERR_INVALIDCALL, D3DERR_NOTAVAILABLE, D3DERR_OUTOFVIDEOMEMORY.

## -remarks

This method returns a fully working device interface, set to the required display mode (or windowed), and allocated with the appropriate back buffers. To begin rendering, the application needs only to create and set a depth buffer (assuming EnableAutoDepthStencil is <b>FALSE</b> in <a href="/windows/desktop/direct3d9/d3dpresent-parameters">D3DPRESENT_PARAMETERS</a>).

When you create a Direct3D device, you supply two different window parameters: a focus window (hFocusWindow) and a device window (the hDeviceWindow in <a href="/windows/desktop/direct3d9/d3dpresent-parameters">D3DPRESENT_PARAMETERS</a>). The purpose of each window is:

<ul>
<li>The focus window alerts Direct3D when an application switches from foreground mode to background mode (via Alt-Tab, a mouse click, or some other method). A single focus window is shared by each device created by an application.</li>
<li>The device window determines the location and size of the back buffer on screen. This is used by Direct3D when the back buffer contents are copied to the front buffer during <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-present">Present</a>.</li>
</ul>
This method should not be run during the handling of WM_CREATE. An application should never pass a window handle to Direct3D while handling WM_CREATE. 
    
    Any call to create, release, or reset the device must be done using the same thread as the window procedure of the focus window.

Note that D3DCREATE_HARDWARE_VERTEXPROCESSING, D3DCREATE_MIXED_VERTEXPROCESSING, and D3DCREATE_SOFTWARE_VERTEXPROCESSING are mutually exclusive flags, and at least one of these vertex processing flags must be specified when calling this method.

Back buffers created as part of the device are only lockable if D3DPRESENTFLAG_LOCKABLE_BACKBUFFER is specified in the presentation parameters. (Multisampled back buffers and depth surfaces are never lockable.)

The methods <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-reset">Reset</a>, <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>, and <a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-testcooperativelevel">TestCooperativeLevel</a> must be called from the same thread that used this method to create a device.

D3DFMT_UNKNOWN can be specified for the windowed mode back buffer format when calling <b>CreateDevice</b>, <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-reset">Reset</a>, and <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createadditionalswapchain">CreateAdditionalSwapChain</a>. This means the application does not have to query the current desktop format before calling <b>CreateDevice</b> for windowed mode. For full-screen mode, the back buffer format must be specified.

If you attempt to create a device on a 0x0 sized window, <b>CreateDevice</b> will fail.

## -see-also

<a href="/windows/desktop/direct3d9/d3ddevice-creation-parameters">D3DDEVICE_CREATION_PARAMETERS</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-direct3dcreate9">Direct3DCreate9</a>



<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3d9">IDirect3D9</a>



<a href="/windows/desktop/direct3d9/multihead">Multihead (Direct3D 9)</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-reset">Reset</a>
