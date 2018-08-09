---
UID: NF:d3d9.IDirect3D9Ex.CreateDeviceEx
title: IDirect3D9Ex::CreateDeviceEx
author: windows-sdk-content
description: Creates a device to represent the display adapter.
old-location: direct3d9\idirect3d9ex_createdeviceex.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3d9ex_createdeviceex.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreateDeviceEx, CreateDeviceEx method [Direct3D 9], CreateDeviceEx method [Direct3D 9],IDirect3D9Ex interface, IDirect3D9Ex interface [Direct3D 9],CreateDeviceEx method, IDirect3D9Ex.CreateDeviceEx, IDirect3D9Ex::CreateDeviceEx, bf3a239e-48e9-f485-78d3-f075bed4ac3a, d3d9/IDirect3D9Ex::CreateDeviceEx, direct3d9.idirect3d9ex_createdeviceex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d9.h
req.include-header: 
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
 - IDirect3D9Ex.CreateDeviceEx
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3D9Ex::CreateDeviceEx


## -description


Creates a device to represent the display adapter.


## -parameters




### -param Adapter [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Ordinal number that denotes the display adapter. <a href="https://msdn.microsoft.com/76f91917-394a-4588-9c83-c35bddb36b8e">D3DADAPTER_DEFAULT</a> is always the primary display adapter.


### -param DeviceType [in]

Type: <b><a href="https://msdn.microsoft.com/2bcdc476-7c42-4152-b107-58366faf2abd">D3DDEVTYPE</a></b>

Specifies the type of device. See <a href="https://msdn.microsoft.com/2bcdc476-7c42-4152-b107-58366faf2abd">D3DDEVTYPE</a>. If the desired device type is not available, the method will fail.


### -param hFocusWindow [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

The focus window alerts Direct3D when an application switches from foreground mode to background mode. For full-screen mode, the window specified must be a top-level window. For windowed mode, this parameter may be <b>NULL</b> only if the hDeviceWindow member of pPresentationParameters is set to a valid, non-<b>NULL</b> value.


### -param BehaviorFlags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Combination of one or more options (see <a href="https://msdn.microsoft.com/91387a2d-3927-4285-a09b-9ce247e6bfdd">D3DCREATE</a>) that control device creation.


### -param pPresentationParameters [in, out]

Type: <b><a href="https://msdn.microsoft.com/d677aeb7-a188-4ddc-b8c9-48e13676e9c8">D3DPRESENT_PARAMETERS</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/d677aeb7-a188-4ddc-b8c9-48e13676e9c8">D3DPRESENT_PARAMETERS</a> structure, describing the presentation parameters for the device to be created. If <i>BehaviorFlags</i> specifies <a href="https://msdn.microsoft.com/91387a2d-3927-4285-a09b-9ce247e6bfdd">D3DCREATE_ADAPTERGROUP_DEVICE</a>, this parameter is an array. Regardless of the number of heads that exist, only one depth/stencil surface is automatically created.

This parameter is both an input and an output parameter. Calling this method may change several members including:

<ul>
<li>If BackBufferCount, BackBufferWidth, and BackBufferHeight are 0 before the method is called, they will be changed when the method returns.</li>
<li>If BackBufferFormat equals <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFMT_UNKNOWN</a> before the method is called, it will be changed when the method returns.</li>
</ul>

### -param pFullscreenDisplayMode [in, out]

Type: <b><a href="https://msdn.microsoft.com/df9d12b9-7acb-435b-9d54-0b095c871f0e">D3DDISPLAYMODEEX</a>*</b>

The display mode for when the device is set to fullscreen. See <a href="https://msdn.microsoft.com/df9d12b9-7acb-435b-9d54-0b095c871f0e">D3DDISPLAYMODEEX</a>. If <i>BehaviorFlags</i> specifies <a href="https://msdn.microsoft.com/91387a2d-3927-4285-a09b-9ce247e6bfdd">D3DCREATE_ADAPTERGROUP_DEVICE</a>, this parameter is an array. This parameter must be <b>NULL</b> for windowed mode.


### -param ppReturnedDeviceInterface [out, retval]

Type: <b><a href="https://msdn.microsoft.com/b2132ee3-5888-4cfe-a7c7-1134c0418a37">IDirect3DDevice9Ex</a>**</b>

Address of a pointer to the returned <a href="https://msdn.microsoft.com/b2132ee3-5888-4cfe-a7c7-1134c0418a37">IDirect3DDevice9Ex</a>, which represents the created device.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns S_OK when rendering device along with swapchain buffers are created successfully. D3DERR_DEVICELOST is returned when any error other than invalid caller input is encountered.




## -see-also




<a href="https://msdn.microsoft.com/68dbd2d4-0a38-47fc-ad3d-4ac209ed98a8">IDirect3D9Ex</a>
 

 

