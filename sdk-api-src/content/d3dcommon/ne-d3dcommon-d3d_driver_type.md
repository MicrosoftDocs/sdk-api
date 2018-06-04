---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# D3D_DRIVER_TYPE enumeration


## -description


Driver type options.


## -enum-fields




### -field D3D_DRIVER_TYPE_UNKNOWN

The driver type is unknown.


### -field D3D_DRIVER_TYPE_HARDWARE

A hardware driver, which implements Direct3D features in hardware. This is the primary driver that you should use in your Direct3D applications because it provides the best performance. A hardware driver uses hardware acceleration (on supported hardware) but can also use software for parts of the pipeline that are not supported in hardware. This driver type is often referred to as a hardware abstraction layer or HAL.


### -field D3D_DRIVER_TYPE_REFERENCE

A reference driver, which is a software implementation that supports every Direct3D feature. A reference driver is designed for accuracy rather than speed and as a result is slow but accurate. The rasterizer portion of the driver does make use of special CPU instructions whenever it can, but it is not intended for retail applications; use it only for feature testing, demonstration of functionality, debugging, or verifying bugs in other drivers. The reference device for this driver is installed by the Windows SDK 8.0 or later and is intended only as a debug aid for development purposes. This driver may be referred to as a REF driver, a reference driver, or a reference rasterizer.

<div class="alert"><b>Note</b>  When you use the REF driver in Windows Store apps,  the REF driver renders correctly but doesn't display any output on the screen. To verify bugs in hardware drivers for Windows Store apps, use <a href="d3d_driver_type.htm">D3D_DRIVER_TYPE_WARP</a> for the WARP driver instead.</div>
<div> </div>

### -field D3D_DRIVER_TYPE_NULL

A NULL driver, which is a reference driver without render capability. This driver is commonly used for debugging non-rendering API calls, it is not appropriate for retail applications. This driver is installed by the DirectX SDK.


### -field D3D_DRIVER_TYPE_SOFTWARE

A software driver, which is a driver implemented completely in software. The software implementation is not intended for a high-performance application due to its very slow performance.


### -field D3D_DRIVER_TYPE_WARP

A WARP driver, which is a high-performance software rasterizer. The rasterizer supports <a href="https://msdn.microsoft.com/afbc1a02-1730-4502-af15-b668412d664c">feature levels</a> 9_1 through level 10_1 with a high performance software implementation. For information about limitations creating a WARP device on certain feature levels, see <a href="https://msdn.microsoft.com/7e022e5d-daa3-48fa-b9fe-4b569220e55e">Limitations Creating WARP and Reference Devices</a>. For more information about using a WARP driver, see <a href="https://msdn.microsoft.com/C40A96EB-64AA-46EB-85A9-7C996ABC8BFE">Windows Advanced Rasterization Platform (WARP) In-Depth Guide</a>.

<div class="alert"><b>Note</b>  The WARP driver that Windows 8 includes supports <a href="overviews_direct3d_11_devices_downlevel_intro.htm">feature levels</a> 9_1 through level 11_1.</div>
<div> </div>
<div class="alert"><b>Note</b>  The WARP driver that Windows 8.1 includes fully supports <a href="overviews_direct3d_11_devices_downlevel_intro.htm">feature level</a> 11_1, including tiled resources, <a href="https://msdn.microsoft.com/7A697B4B-4D0E-46F9-BC82-860FB91B365B">IDXGIDevice3::Trim</a>, shared BCn surfaces, minblend, and map default. </div>
<div> </div>

## -remarks



The driver type is required when calling <a href="https://msdn.microsoft.com/d1c85ec0-84a8-41ff-9cbe-f47bbaa5863b">D3D11CreateDevice</a> or <a href="https://msdn.microsoft.com/84d73e8c-f13c-4343-91de-57f9f8a0ad96">D3D11CreateDeviceAndSwapChain</a>.




## -see-also




<a href="https://msdn.microsoft.com/002154d5-74a6-48fb-b55f-8687e4505fc7">Common Version Enumerations</a>
 

 

