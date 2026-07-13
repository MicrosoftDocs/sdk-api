---
UID: NE:d3d11.D3D11_CREATE_DEVICE_FLAG
title: D3D11_CREATE_DEVICE_FLAG (d3d11.h)
description: Describes parameters that are used to create a device.
helpviewer_keywords: ["D3D11_CREATE_DEVICE_BGRA_SUPPORT","D3D11_CREATE_DEVICE_DEBUG","D3D11_CREATE_DEVICE_DEBUGGABLE","D3D11_CREATE_DEVICE_DISABLE_GPU_TIMEOUT","D3D11_CREATE_DEVICE_FLAG","D3D11_CREATE_DEVICE_FLAG enumeration [Direct3D 11]","D3D11_CREATE_DEVICE_PREVENT_ALTERING_LAYER_SETTINGS_FROM_REGISTRY","D3D11_CREATE_DEVICE_PREVENT_INTERNAL_THREADING_OPTIMIZATIONS","D3D11_CREATE_DEVICE_SINGLETHREADED","D3D11_CREATE_DEVICE_SWITCH_TO_REF","D3D11_CREATE_DEVICE_VIDEO_SUPPORT","d3d11/D3D11_CREATE_DEVICE_BGRA_SUPPORT","d3d11/D3D11_CREATE_DEVICE_DEBUG","d3d11/D3D11_CREATE_DEVICE_DEBUGGABLE","d3d11/D3D11_CREATE_DEVICE_DISABLE_GPU_TIMEOUT","d3d11/D3D11_CREATE_DEVICE_FLAG","d3d11/D3D11_CREATE_DEVICE_PREVENT_ALTERING_LAYER_SETTINGS_FROM_REGISTRY","d3d11/D3D11_CREATE_DEVICE_PREVENT_INTERNAL_THREADING_OPTIMIZATIONS","d3d11/D3D11_CREATE_DEVICE_SINGLETHREADED","d3d11/D3D11_CREATE_DEVICE_SWITCH_TO_REF","d3d11/D3D11_CREATE_DEVICE_VIDEO_SUPPORT","d68526ea-ccc4-6cc8-c252-eefe99541f51","direct3d11.d3d11_create_device_flag"]
old-location: direct3d11\d3d11_create_device_flag.htm
tech.root: direct3d11
ms.assetid: 580c784a-17de-495c-9159-833f858ad155
ms.date: 12/05/2018
ms.keywords: D3D11_CREATE_DEVICE_BGRA_SUPPORT, D3D11_CREATE_DEVICE_DEBUG, D3D11_CREATE_DEVICE_DEBUGGABLE, D3D11_CREATE_DEVICE_DISABLE_GPU_TIMEOUT, D3D11_CREATE_DEVICE_FLAG, D3D11_CREATE_DEVICE_FLAG enumeration [Direct3D 11], D3D11_CREATE_DEVICE_PREVENT_ALTERING_LAYER_SETTINGS_FROM_REGISTRY, D3D11_CREATE_DEVICE_PREVENT_INTERNAL_THREADING_OPTIMIZATIONS, D3D11_CREATE_DEVICE_SINGLETHREADED, D3D11_CREATE_DEVICE_SWITCH_TO_REF, D3D11_CREATE_DEVICE_VIDEO_SUPPORT, d3d11/D3D11_CREATE_DEVICE_BGRA_SUPPORT, d3d11/D3D11_CREATE_DEVICE_DEBUG, d3d11/D3D11_CREATE_DEVICE_DEBUGGABLE, d3d11/D3D11_CREATE_DEVICE_DISABLE_GPU_TIMEOUT, d3d11/D3D11_CREATE_DEVICE_FLAG, d3d11/D3D11_CREATE_DEVICE_PREVENT_ALTERING_LAYER_SETTINGS_FROM_REGISTRY, d3d11/D3D11_CREATE_DEVICE_PREVENT_INTERNAL_THREADING_OPTIMIZATIONS, d3d11/D3D11_CREATE_DEVICE_SINGLETHREADED, d3d11/D3D11_CREATE_DEVICE_SWITCH_TO_REF, d3d11/D3D11_CREATE_DEVICE_VIDEO_SUPPORT, d68526ea-ccc4-6cc8-c252-eefe99541f51, direct3d11.d3d11_create_device_flag
req.header: d3d11.h
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
req.typenames: D3D11_CREATE_DEVICE_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_CREATE_DEVICE_FLAG
 - d3d11/D3D11_CREATE_DEVICE_FLAG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_CREATE_DEVICE_FLAG
---

# D3D11_CREATE_DEVICE_FLAG enumeration


## -description

Describes parameters that are used to create a device.

## -enum-fields

### -field D3D11_CREATE_DEVICE_SINGLETHREADED:0x1

Use this flag if your application will only call methods of Direct3D 11 interfaces from a single thread. By default, the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a> object is  <a href="/windows/desktop/direct3d11/overviews-direct3d-11-render-multi-thread-differences">thread-safe</a>. 
        By using this flag, you can increase performance. However, if you use this flag and your application calls methods of Direct3D 11 interfaces from multiple threads, undefined behavior might result.

### -field D3D11_CREATE_DEVICE_DEBUG:0x2

Creates a device that supports the <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers">debug layer</a>. 

To use this flag, you must have D3D11*SDKLayers.dll installed; otherwise, device creation fails. To get D3D11_1SDKLayers.dll, install the SDK for Windows 8.

### -field D3D11_CREATE_DEVICE_SWITCH_TO_REF:0x4

<div class="alert"><b>Note</b>  This flag is not supported in Direct3D 11.</div>
<div> </div>

### -field D3D11_CREATE_DEVICE_PREVENT_INTERNAL_THREADING_OPTIMIZATIONS:0x8

Prevents multiple threads from being created. When this flag is used with a <a href="/windows/desktop/direct3darticles/directx-warp">Windows Advanced Rasterization Platform (WARP)</a> device, no additional threads will be created by WARP 
        and all rasterization will occur on the calling thread. This flag is not recommended for general use. See remarks.

### -field D3D11_CREATE_DEVICE_BGRA_SUPPORT:0x20

Creates a device that supports BGRA formats (<a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT_B8G8R8A8_UNORM</a> and <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT_B8G8R8A8_UNORM_SRGB</a>). All 10level9 and higher hardware with WDDM 1.1+ drivers support BGRA formats. 

<div class="alert"><b>Note</b>  Required for Direct2D interoperability with Direct3D resources.</div>
<div> </div>

### -field D3D11_CREATE_DEVICE_DEBUGGABLE:0x40

Causes the device and driver to keep information that you can use for shader debugging.  The exact impact from this flag will vary from driver to driver.  

To use this flag, you must have D3D11_1SDKLayers.dll installed; otherwise, device creation fails. The created device supports the <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers">debug layer</a>. To get D3D11_1SDKLayers.dll, install the SDK for Windows 8.

If you use this flag and the current driver does not support shader debugging, device creation fails. Shader debugging requires a driver that is implemented to the WDDM for Windows 8 (WDDM 1.2).

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.1.

### -field D3D11_CREATE_DEVICE_PREVENT_ALTERING_LAYER_SETTINGS_FROM_REGISTRY:0x80

Causes the Direct3D runtime to ignore registry settings that turn on the <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers">debug layer</a>. You can turn on the debug layer by using the <a href="/previous-versions/bb219725(v=vs.85)">DirectX Control Panel</a> that was included as part of the DirectX SDK. We shipped the last version of the DirectX SDK in June 2010; you can download it from the <a href="https://www.microsoft.com/download/en/details.aspx?id=6812">Microsoft Download Center</a>. You can set this flag in your app, typically in release builds only, to prevent end users from using the <a href="/previous-versions/bb219725(v=vs.85)">DirectX Control Panel</a> to monitor how the app uses Direct3D.

<div class="alert"><b>Note</b>  You can also set this flag in your app to prevent Direct3D debugging tools, such as Visual Studio Ultimate 2012, from hooking your app.</div>
<div> </div>
<b>Windows 8.1:  </b>This flag doesn't prevent Visual Studio 2013 and later running on Windows 8.1 and later from hooking your app; instead use <a href="/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-isannotationenabled">ID3D11DeviceContext2::IsAnnotationEnabled</a>. This flag still prevents Visual Studio 2013 and later running on Windows 8 and earlier from hooking your app. 

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.1.

### -field D3D11_CREATE_DEVICE_DISABLE_GPU_TIMEOUT:0x100

Use this flag if the device will produce GPU workloads that take more than two seconds to complete, and you want the operating system to allow them to successfully finish. If this flag is not set, the operating system performs <a href="/windows-hardware/drivers/display/timeout-detection-and-recovery">timeout detection and recovery</a> when it detects a GPU packet that took more than two seconds to execute. If this flag is set, the operating system allows such a long running packet to execute without resetting the GPU. We recommend not to set this flag if your device needs to be highly responsive so that the operating system can detect and recover from GPU timeouts. We recommend to set this flag if your device needs to perform time consuming background tasks such as compute, image recognition, and video encoding to allow such tasks to successfully finish.

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.1.

### -field D3D11_CREATE_DEVICE_VIDEO_SUPPORT:0x800

Forces the creation of the Direct3D device to fail if the display driver is not implemented to the WDDM for Windows 8 (WDDM 1.2). When the display driver is not implemented to WDDM 1.2, only a Direct3D device that is created with <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> 9.1, 9.2, or 9.3 supports video; therefore, if this flag is set, the runtime creates the Direct3D device only for feature level 9.1, 9.2, or 9.3. We recommend not to specify this flag for applications that want to favor Direct3D capability over video. If feature level 10 and higher is available, the runtime will use that feature level regardless of video support.

If this flag is set, device creation on the Basic Render Device (BRD) will succeed regardless of the BRD's missing support for video decode. This is because the Media Foundation video stack operates in software mode on BRD. In this situation, if you force the video stack to create the Direct3D device twice (create the device once with this flag, next discover BRD, then again create the device without the flag), you actually degrade performance.

If you attempt to create a Direct3D device with driver type <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type">D3D_DRIVER_TYPE_NULL</a>, <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type">D3D_DRIVER_TYPE_REFERENCE</a>, or <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type">D3D_DRIVER_TYPE_SOFTWARE</a>, device creation fails at any <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> because none of the associated drivers provide video capability. If you attempt to create a Direct3D device with driver type <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type">D3D_DRIVER_TYPE_WARP</a>, device creation succeeds to allow software fallback for video.

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.1.

## -remarks

Device creation flags are used by <a href="/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice">D3D11CreateDevice</a> and <a href="/windows/desktop/api/d3d11/nf-d3d11-d3d11createdeviceandswapchain">D3D11CreateDeviceAndSwapChain</a>.

An application might dynamically create (and destroy) threads to improve performance especially on a machine with multiple CPU cores. There may be cases, however, when an application needs to prevent extra threads from being created. This can happen when you want to simplify debugging, profile code or develop a tool for instance. For these cases, use <b>D3D11_CREATE_DEVICE_PREVENT_INTERNAL_THREADING_OPTIMIZATIONS</b> to request that the runtime and video driver not create any additional threads that might interfere with the application.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-enums">Core Enumerations</a>
