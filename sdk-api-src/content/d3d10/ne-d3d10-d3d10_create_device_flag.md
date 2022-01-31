---
UID: NE:d3d10.D3D10_CREATE_DEVICE_FLAG
title: D3D10_CREATE_DEVICE_FLAG (d3d10.h)
description: Device creation flags.
helpviewer_keywords: ["3a55fe0a-90a0-6ccb-7720-5039c4fbf12b","D3D10_CREATE_DEVICE_ALLOW_NULL_FROM_MAP","D3D10_CREATE_DEVICE_BGRA_SUPPORT","D3D10_CREATE_DEVICE_DEBUG","D3D10_CREATE_DEVICE_DEBUGGABLE","D3D10_CREATE_DEVICE_FLAG","D3D10_CREATE_DEVICE_FLAG enumeration [Direct3D 10]","D3D10_CREATE_DEVICE_PREVENT_ALTERING_LAYER_SETTINGS_FROM_REGISTRY","D3D10_CREATE_DEVICE_PREVENT_INTERNAL_THREADING_OPTIMIZATIONS","D3D10_CREATE_DEVICE_SINGLETHREADED","D3D10_CREATE_DEVICE_STRICT_VALIDATION","D3D10_CREATE_DEVICE_SWITCH_TO_REF","d3d10/D3D10_CREATE_DEVICE_ALLOW_NULL_FROM_MAP","d3d10/D3D10_CREATE_DEVICE_BGRA_SUPPORT","d3d10/D3D10_CREATE_DEVICE_DEBUG","d3d10/D3D10_CREATE_DEVICE_DEBUGGABLE","d3d10/D3D10_CREATE_DEVICE_FLAG","d3d10/D3D10_CREATE_DEVICE_PREVENT_ALTERING_LAYER_SETTINGS_FROM_REGISTRY","d3d10/D3D10_CREATE_DEVICE_PREVENT_INTERNAL_THREADING_OPTIMIZATIONS","d3d10/D3D10_CREATE_DEVICE_SINGLETHREADED","d3d10/D3D10_CREATE_DEVICE_STRICT_VALIDATION","d3d10/D3D10_CREATE_DEVICE_SWITCH_TO_REF","direct3d10.d3d10_create_device_flag"]
old-location: direct3d10\d3d10_create_device_flag.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_create_device_flag.htm
ms.date: 12/05/2018
ms.keywords: 3a55fe0a-90a0-6ccb-7720-5039c4fbf12b, D3D10_CREATE_DEVICE_ALLOW_NULL_FROM_MAP, D3D10_CREATE_DEVICE_BGRA_SUPPORT, D3D10_CREATE_DEVICE_DEBUG, D3D10_CREATE_DEVICE_DEBUGGABLE, D3D10_CREATE_DEVICE_FLAG, D3D10_CREATE_DEVICE_FLAG enumeration [Direct3D 10], D3D10_CREATE_DEVICE_PREVENT_ALTERING_LAYER_SETTINGS_FROM_REGISTRY, D3D10_CREATE_DEVICE_PREVENT_INTERNAL_THREADING_OPTIMIZATIONS, D3D10_CREATE_DEVICE_SINGLETHREADED, D3D10_CREATE_DEVICE_STRICT_VALIDATION, D3D10_CREATE_DEVICE_SWITCH_TO_REF, d3d10/D3D10_CREATE_DEVICE_ALLOW_NULL_FROM_MAP, d3d10/D3D10_CREATE_DEVICE_BGRA_SUPPORT, d3d10/D3D10_CREATE_DEVICE_DEBUG, d3d10/D3D10_CREATE_DEVICE_DEBUGGABLE, d3d10/D3D10_CREATE_DEVICE_FLAG, d3d10/D3D10_CREATE_DEVICE_PREVENT_ALTERING_LAYER_SETTINGS_FROM_REGISTRY, d3d10/D3D10_CREATE_DEVICE_PREVENT_INTERNAL_THREADING_OPTIMIZATIONS, d3d10/D3D10_CREATE_DEVICE_SINGLETHREADED, d3d10/D3D10_CREATE_DEVICE_STRICT_VALIDATION, d3d10/D3D10_CREATE_DEVICE_SWITCH_TO_REF, direct3d10.d3d10_create_device_flag
req.header: d3d10.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D3D10_CREATE_DEVICE_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_CREATE_DEVICE_FLAG
 - d3d10/D3D10_CREATE_DEVICE_FLAG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_CREATE_DEVICE_FLAG
---

# D3D10_CREATE_DEVICE_FLAG enumeration


## -description

Device creation flags.

## -enum-fields

### -field D3D10_CREATE_DEVICE_SINGLETHREADED:0x1

Use this flag if an application will only be calling D3D10 from a single thread. If this flag is not specified, the default behavior of D3D10 
        is to enter a lock during each API call to prevent multiple threads altering internal state. By using this flag no locks will be taken which can 
        slightly increase performance, but could result in undefine behavior if D3D10 is called from multiple threads.

### -field D3D10_CREATE_DEVICE_DEBUG:0x2

Create a device that supports the <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-api-features-layers">debug layer</a>.

### -field D3D10_CREATE_DEVICE_SWITCH_TO_REF:0x4

Create both a software (REF) and hardware (HAL) version of the device simultaneously, which allows an application to switch to a 
        reference device to enable debugging. See <a href="/windows/desktop/api/d3d10sdklayers/nn-d3d10sdklayers-id3d10switchtoref">ID3D10SwitchToRef Interface</a> for more information.

### -field D3D10_CREATE_DEVICE_PREVENT_INTERNAL_THREADING_OPTIMIZATIONS:0x8

Prevents multiple threads from being created. When this flag is used with a WARP device, no additional threads will be created by WARP and all
        rasterization will occur on the calling thread. This flag is not recommended for general use. See remarks.

### -field D3D10_CREATE_DEVICE_ALLOW_NULL_FROM_MAP:0x10

Return a <b>NULL</b> pointer instead of triggering an exception on memory exhaustion during invocations to Map.  
        Without this flag an exception will be raised on memory exhaustion.  Only valid on Windows 7.

### -field D3D10_CREATE_DEVICE_BGRA_SUPPORT:0x20

Causes device creation to fail if BGRA support is not available.

BGRA support enables the following formats.

<ul>
<li>DXGI_FORMAT_B8G8R8A8_TYPELESS</li>
<li>DXGI_FORMAT_B8G8R8A8_UNORM</li>
<li>DXGI_FORMAT_B8G8R8A8_UNORM_SRGB</li>
<li>DXGI_FORMAT_B8G8R8X8_TYPELESS</li>
<li>DXGI_FORMAT_B8G8R8X8_UNORM</li>
<li>DXGI_FORMAT_B8G8R8X8_UNORM_SRGB</li>
</ul>
D3D10_CREATE_DEVICE_BGRA_SUPPORT is only relevant when a device is created with <a href="/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1">D3D10CreateDevice1</a> 
          or <a href="/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdeviceandswapchain1">D3D10CreateDeviceAndSwapChain1</a> using the <b>D3D10_FEATURE_LEVEL_10_0</b> or <b>D3D10_FEATURE_LEVEL_10_1</b> 
          feature levels, the flag will be ignored when a device is created with other feature levels.

Note that BGRA support may be present even if the application didn't specify D3D10_CREATE_DEVICE_BGRA_SUPPORT. 
          The flag merely causes device creation to fail if BGRA support isn't available.

D3D10_CREATE_DEVICE_BGRA_SUPPORT is only valid on Windows 7, Windows Server 2008 R2, and updated Windows Vista (KB971644) systems.

### -field D3D10_CREATE_DEVICE_PREVENT_ALTERING_LAYER_SETTINGS_FROM_REGISTRY:0x80

Causes the Direct3D runtime to ignore registry settings that turn on the <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-api-features-layers">debug layer</a>. You can turn on the debug layer by using the <a href="/previous-versions/bb219725(v=vs.85)">DirectX Control Panel</a> that was included as part of the DirectX SDK. We shipped the last version of the DirectX SDK in June 2010; you can download it from the <a href="https://www.microsoft.com/download/en/details.aspx?id=6812">Microsoft Download Center</a>. You can set this flag in your app, typically in release builds only, to prevent end users from using the <a href="/previous-versions/bb219725(v=vs.85)">DirectX Control Panel</a> to monitor how the app uses Direct3D.

<div class="alert"><b>Note</b>  You can also set this flag in your app to prevent Direct3D debugging tools, such as Visual Studio Ultimate 2012, from hooking your app.</div>
<div> </div>
<b>Windows 8.1:  </b>This flag doesn't prevent Visual Studio 2013 and later running on Windows 8.1 and later from hooking your app. But, this flag still prevents Visual Studio 2013 and later running on Windows 8 and earlier from hooking your app. 

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.1.

### -field D3D10_CREATE_DEVICE_STRICT_VALIDATION:0x200

Reserved. This flag is currently not supported. Do not use.

### -field D3D10_CREATE_DEVICE_DEBUGGABLE:0x400

Causes the device and driver to keep information that you can use for shader debugging.  The exact impact from this flag will vary from driver to driver.  To use this flag, you must have D3D11_1SDKLayers.dll installed; otherwise, device creation fails. The created device supports the <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-api-features-layers">debug layer</a>. To get D3D11_1SDKLayers.dll, you must install the SDK for Windows 8.

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.1.

## -remarks

Device creation flags are used by <a href="/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice">D3D10CreateDevice</a> and <a href="/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdeviceandswapchain">D3D10CreateDeviceAndSwapChain</a>.

An application might dynamically create (and destroy) threads to improve performance especially on a machine with multiple CPU cores. 
      There may be cases, however, when an application needs to prevent extra threads from being created. This can happen when you want to simplify 
      debugging, profile code or develop a tool for instance. For these cases, use D3D10_CREATE_DEVICE_PREVENT_INTERNAL_THREADING_OPTIMIZATIONS to request 
      that the runtime and video driver not create any additional threads that might interfere with the application.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-enums">Core Enumerations</a>
