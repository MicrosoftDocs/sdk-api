---
UID: NE:d3dcommon.D3D_DRIVER_TYPE
title: D3D_DRIVER_TYPE (d3dcommon.h)
description: Driver type options.
helpviewer_keywords: ["5f2e6561-a389-e8e8-0b80-96db66f58139","D3D_DRIVER_TYPE","D3D_DRIVER_TYPE enumeration [Direct3D 11]","D3D_DRIVER_TYPE_HARDWARE","D3D_DRIVER_TYPE_NULL","D3D_DRIVER_TYPE_REFERENCE","D3D_DRIVER_TYPE_SOFTWARE","D3D_DRIVER_TYPE_UNKNOWN","D3D_DRIVER_TYPE_WARP","d3dcommon/D3D_DRIVER_TYPE","d3dcommon/D3D_DRIVER_TYPE_HARDWARE","d3dcommon/D3D_DRIVER_TYPE_NULL","d3dcommon/D3D_DRIVER_TYPE_REFERENCE","d3dcommon/D3D_DRIVER_TYPE_SOFTWARE","d3dcommon/D3D_DRIVER_TYPE_UNKNOWN","d3dcommon/D3D_DRIVER_TYPE_WARP","direct3d11.d3d_driver_type"]
old-location: direct3d11\d3d_driver_type.htm
tech.root: direct3d11
ms.assetid: ceeec7d6-4bdc-488c-80a8-6c5e11986d6a
ms.date: 12/05/2018
ms.keywords: 5f2e6561-a389-e8e8-0b80-96db66f58139, D3D_DRIVER_TYPE, D3D_DRIVER_TYPE enumeration [Direct3D 11], D3D_DRIVER_TYPE_HARDWARE, D3D_DRIVER_TYPE_NULL, D3D_DRIVER_TYPE_REFERENCE, D3D_DRIVER_TYPE_SOFTWARE, D3D_DRIVER_TYPE_UNKNOWN, D3D_DRIVER_TYPE_WARP, d3dcommon/D3D_DRIVER_TYPE, d3dcommon/D3D_DRIVER_TYPE_HARDWARE, d3dcommon/D3D_DRIVER_TYPE_NULL, d3dcommon/D3D_DRIVER_TYPE_REFERENCE, d3dcommon/D3D_DRIVER_TYPE_SOFTWARE, d3dcommon/D3D_DRIVER_TYPE_UNKNOWN, d3dcommon/D3D_DRIVER_TYPE_WARP, direct3d11.d3d_driver_type
req.header: d3dcommon.h
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
req.typenames: D3D_DRIVER_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D_DRIVER_TYPE
 - d3dcommon/D3D_DRIVER_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3DCommon.h
api_name:
 - D3D_DRIVER_TYPE
---

## -description

Driver type options.

> [!NOTE]
> For programming with Direct3D 10, this API has a type alias that begins `D3D10_` instead of `D3D_`. These Direct3D 10 type aliases are defined in `d3d10.h`, `d3d10misc.h`, and `d3d10shader.h`.

## -enum-fields

### -field D3D_DRIVER_TYPE_UNKNOWN:0

The driver type is unknown.

### -field D3D_DRIVER_TYPE_HARDWARE

A hardware driver, which implements Direct3D features in hardware. This is the primary driver that you should use in your Direct3D applications because it provides the best performance. A hardware driver uses hardware acceleration (on supported hardware) but can also use software for parts of the pipeline that are not supported in hardware. This driver type is often referred to as a hardware abstraction layer or HAL.

### -field D3D_DRIVER_TYPE_REFERENCE

A reference driver, which is a software implementation that supports every Direct3D feature. A reference driver is designed for accuracy rather than speed and as a result is slow but accurate. The rasterizer portion of the driver does make use of special CPU instructions whenever it can, but it is not intended for retail applications; use it only for feature testing, demonstration of functionality, debugging, or verifying bugs in other drivers. The reference device for this driver is installed by the Windows SDK 8.0 or later and is intended only as a debug aid for development purposes. This driver may be referred to as a REF driver, a reference driver, or a reference rasterizer.

<div class="alert"><b>Note</b>  When you use the REF driver in Windows Store apps,  the REF driver renders correctly but doesn't display any output on the screen. To verify bugs in hardware drivers for Windows Store apps, use <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type">D3D_DRIVER_TYPE_WARP</a> for the WARP driver instead.</div>
<div> </div>

### -field D3D_DRIVER_TYPE_NULL

A NULL driver, which is a reference driver without render capability. This driver is commonly used for debugging non-rendering API calls, it is not appropriate for retail applications. This driver is installed by the DirectX SDK.

### -field D3D_DRIVER_TYPE_SOFTWARE

A software driver, which is a driver implemented completely in software. The software implementation is not intended for a high-performance application due to its very slow performance.

### -field D3D_DRIVER_TYPE_WARP

A WARP driver, which is a high-performance software rasterizer. The rasterizer supports <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level">feature levels</a> 9_1 through level 10_1 with a high performance software implementation. For information about limitations creating a WARP device on certain feature levels, see <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-limitations">Limitations Creating WARP and Reference Devices</a>. For more information about using a WARP driver, see <a href="/windows/desktop/direct3darticles/directx-warp">Windows Advanced Rasterization Platform (WARP) In-Depth Guide</a>.

<div class="alert"><b>Note</b>  The WARP driver that Windows 8 includes supports <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature levels</a> 9_1 through level 11_1.</div>
<div> </div>
<div class="alert"><b>Note</b>  The WARP driver that Windows 8.1 includes fully supports <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> 11_1, including tiled resources, <a href="/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgidevice3-trim">IDXGIDevice3::Trim</a>, shared BCn surfaces, minblend, and map default. </div>
<div> </div>

## -remarks

The driver type is required when calling <a href="/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice">D3D11CreateDevice</a> or <a href="/windows/desktop/api/d3d11/nf-d3d11-d3d11createdeviceandswapchain">D3D11CreateDeviceAndSwapChain</a>.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-common-enumerations">Common Version Enumerations</a>
