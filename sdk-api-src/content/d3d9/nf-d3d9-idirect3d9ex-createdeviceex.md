---
UID: NF:d3d9.IDirect3D9Ex.CreateDeviceEx
title: IDirect3D9Ex::CreateDeviceEx
author: windows-sdk-content
description: Creates a device to represent the display adapter.
old-location: direct3d9\idirect3d9ex_createdeviceex.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3d9ex_createdeviceex.htm
ms.author: windowssdkdev
ms.date: 04/10/2018
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

Ordinal number that denotes the display adapter. <a href="https://msdn.microsoft.com/library/Bb172504(v=VS.85).aspx">D3DADAPTER_DEFAULT</a> is always the primary display adapter.


### -param DeviceType [in]

Type: <b><a href="https://msdn.microsoft.com/library/Bb172547(v=VS.85).aspx">D3DDEVTYPE</a></b>

Specifies the type of device. See <a href="https://msdn.microsoft.com/library/Bb172547(v=VS.85).aspx">D3DDEVTYPE</a>. If the desired device type is not available, the method will fail.


### -param hFocusWindow [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

The focus window alerts Direct3D when an application switches from foreground mode to background mode. For full-screen mode, the window specified must be a top-level window. For windowed mode, this parameter may be <b>NULL</b> only if the hDeviceWindow member of pPresentationParameters is set to a valid, non-<b>NULL</b> value.


### -param BehaviorFlags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Combination of one or more options (see <a href="https://msdn.microsoft.com/library/Bb172527(v=VS.85).aspx">D3DCREATE</a>) that control device creation.


### -param pPresentationParameters [in, out]

Type: <b><a href="https://msdn.microsoft.com/library/Bb172588(v=VS.85).aspx">D3DPRESENT_PARAMETERS</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/library/Bb172588(v=VS.85).aspx">D3DPRESENT_PARAMETERS</a> structure, describing the presentation parameters for the device to be created. If <i>BehaviorFlags</i> specifies <a href="https://msdn.microsoft.com/library/Bb172527(v=VS.85).aspx">D3DCREATE_ADAPTERGROUP_DEVICE</a>, this parameter is an array. Regardless of the number of heads that exist, only one depth/stencil surface is automatically created.

This parameter is both an input and an output parameter. Calling this method may change several members including:

<ul>
<li>If BackBufferCount, BackBufferWidth, and BackBufferHeight are 0 before the method is called, they will be changed when the method returns.</li>
<li>If BackBufferFormat equals <a href="https://msdn.microsoft.com/library/Bb172558(v=VS.85).aspx">D3DFMT_UNKNOWN</a> before the method is called, it will be changed when the method returns.</li>
</ul>

### -param pFullscreenDisplayMode [in, out]

Type: <b><a href="https://msdn.microsoft.com/library/Bb172549(v=VS.85).aspx">D3DDISPLAYMODEEX</a>*</b>

The display mode for when the device is set to fullscreen. See <a href="https://msdn.microsoft.com/library/Bb172549(v=VS.85).aspx">D3DDISPLAYMODEEX</a>. If <i>BehaviorFlags</i> specifies <a href="https://msdn.microsoft.com/library/Bb172527(v=VS.85).aspx">D3DCREATE_ADAPTERGROUP_DEVICE</a>, this parameter is an array. This parameter must be <b>NULL</b> for windowed mode.


### -param ppReturnedDeviceInterface [out, retval]

Type: <b><a href="https://msdn.microsoft.com/library/Bb174337(v=VS.85).aspx">IDirect3DDevice9Ex</a>**</b>

Address of a pointer to the returned <a href="https://msdn.microsoft.com/library/Bb174337(v=VS.85).aspx">IDirect3DDevice9Ex</a>, which represents the created device.


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns S_OK when rendering device along with swapchain buffers are created successfully. D3DERR_DEVICELOST is returned when any error other than invalid caller input is encountered.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb174301(v=VS.85).aspx">IDirect3D9Ex</a>
 

 

