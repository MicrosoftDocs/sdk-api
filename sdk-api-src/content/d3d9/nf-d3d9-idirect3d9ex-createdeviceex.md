---
UID: NF:d3d9.IDirect3D9Ex.CreateDeviceEx
title: IDirect3D9Ex::CreateDeviceEx (d3d9.h)
description: Creates a device to represent the display adapter. (IDirect3D9Ex.CreateDeviceEx)
helpviewer_keywords: ["CreateDeviceEx","CreateDeviceEx method [Direct3D 9]","CreateDeviceEx method [Direct3D 9]","IDirect3D9Ex interface","IDirect3D9Ex interface [Direct3D 9]","CreateDeviceEx method","IDirect3D9Ex.CreateDeviceEx","IDirect3D9Ex::CreateDeviceEx","bf3a239e-48e9-f485-78d3-f075bed4ac3a","d3d9/IDirect3D9Ex::CreateDeviceEx","direct3d9.idirect3d9ex_createdeviceex"]
old-location: direct3d9\idirect3d9ex_createdeviceex.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3d9ex_createdeviceex.htm
ms.date: 12/05/2018
ms.keywords: CreateDeviceEx, CreateDeviceEx method [Direct3D 9], CreateDeviceEx method [Direct3D 9],IDirect3D9Ex interface, IDirect3D9Ex interface [Direct3D 9],CreateDeviceEx method, IDirect3D9Ex.CreateDeviceEx, IDirect3D9Ex::CreateDeviceEx, bf3a239e-48e9-f485-78d3-f075bed4ac3a, d3d9/IDirect3D9Ex::CreateDeviceEx, direct3d9.idirect3d9ex_createdeviceex
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
req.lib: D3D9.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirect3D9Ex::CreateDeviceEx
 - d3d9/IDirect3D9Ex::CreateDeviceEx
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
 - IDirect3D9Ex.CreateDeviceEx
---

# IDirect3D9Ex::CreateDeviceEx


## -description

Creates a device to represent the display adapter.

## -parameters

### -param Adapter [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Ordinal number that denotes the display adapter. <a href="/windows/desktop/direct3d9/d3dadapter-default">D3DADAPTER_DEFAULT</a> is always the primary display adapter.

### -param DeviceType [in]

Type: <b><a href="/windows/desktop/direct3d9/d3ddevtype">D3DDEVTYPE</a></b>

Specifies the type of device. See <a href="/windows/desktop/direct3d9/d3ddevtype">D3DDEVTYPE</a>. If the desired device type is not available, the method will fail.

### -param hFocusWindow [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

The focus window alerts Direct3D when an application switches from foreground mode to background mode. For full-screen mode, the window specified must be a top-level window. For windowed mode, this parameter may be <b>NULL</b> only if the hDeviceWindow member of pPresentationParameters is set to a valid, non-<b>NULL</b> value.

### -param BehaviorFlags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Combination of one or more options (see <a href="/windows/desktop/direct3d9/d3dcreate">D3DCREATE</a>) that control device creation.

### -param pPresentationParameters [in, out]

Type: <b><a href="/windows/desktop/direct3d9/d3dpresent-parameters">D3DPRESENT_PARAMETERS</a>*</b>

Pointer to a <a href="/windows/desktop/direct3d9/d3dpresent-parameters">D3DPRESENT_PARAMETERS</a> structure, describing the presentation parameters for the device to be created. If <i>BehaviorFlags</i> specifies <a href="/windows/desktop/direct3d9/d3dcreate">D3DCREATE_ADAPTERGROUP_DEVICE</a>, this parameter is an array. Regardless of the number of heads that exist, only one depth/stencil surface is automatically created.

This parameter is both an input and an output parameter. Calling this method may change several members including:

<ul>
<li>If BackBufferCount, BackBufferWidth, and BackBufferHeight are 0 before the method is called, they will be changed when the method returns.</li>
<li>If BackBufferFormat equals <a href="/windows/desktop/direct3d9/d3dformat">D3DFMT_UNKNOWN</a> before the method is called, it will be changed when the method returns.</li>
</ul>

### -param pFullscreenDisplayMode [in, out]

Type: <b><a href="/windows/desktop/direct3d9/d3ddisplaymodeex">D3DDISPLAYMODEEX</a>*</b>

The display mode for when the device is set to fullscreen. See <a href="/windows/desktop/direct3d9/d3ddisplaymodeex">D3DDISPLAYMODEEX</a>. If <i>BehaviorFlags</i> specifies <a href="/windows/desktop/direct3d9/d3dcreate">D3DCREATE_ADAPTERGROUP_DEVICE</a>, this parameter is an array. This parameter must be <b>NULL</b> for windowed mode.

### -param ppReturnedDeviceInterface [out, retval]

Type: <b><a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex">IDirect3DDevice9Ex</a>**</b>

Address of a pointer to the returned <a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex">IDirect3DDevice9Ex</a>, which represents the created device.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns S_OK when rendering device along with swapchain buffers are created successfully. D3DERR_DEVICELOST is returned when any error other than invalid caller input is encountered.

## -see-also

<a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex">IDirect3D9Ex</a>
