---
UID: NE:d3d10misc.D3D10_DRIVER_TYPE
title: D3D10_DRIVER_TYPE (d3d10misc.h)
author: windows-sdk-content
description: The device-driver type.
old-location: direct3d10\d3d10_driver_type.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_driver_type.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 9306ea32-4e52-b274-5c1d-a1782db6ba9e, D3D10_DRIVER_TYPE, D3D10_DRIVER_TYPE enumeration [Direct3D 10], D3D10_DRIVER_TYPE_HARDWARE, D3D10_DRIVER_TYPE_NULL, D3D10_DRIVER_TYPE_REFERENCE, D3D10_DRIVER_TYPE_SOFTWARE, D3D10_DRIVER_TYPE_WARP, d3d10misc/D3D10_DRIVER_TYPE, d3d10misc/D3D10_DRIVER_TYPE_HARDWARE, d3d10misc/D3D10_DRIVER_TYPE_NULL, d3d10misc/D3D10_DRIVER_TYPE_REFERENCE, d3d10misc/D3D10_DRIVER_TYPE_SOFTWARE, d3d10misc/D3D10_DRIVER_TYPE_WARP, direct3d10.d3d10_driver_type
ms.topic: enum
f1_keywords: 
 - "d3d10misc/D3D10_DRIVER_TYPE"
req.header: d3d10misc.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10misc.h
api_name:
 - D3D10_DRIVER_TYPE
targetos: Windows
req.typenames: D3D10_DRIVER_TYPE
req.redist: 
ms.custom: 19H1
---

# D3D10_DRIVER_TYPE enumeration


## -description


The device-driver type.


## -enum-fields




### -field D3D10_DRIVER_TYPE_HARDWARE

A hardware device; commonly called a HAL device.


### -field D3D10_DRIVER_TYPE_REFERENCE

A reference device; commonly called a REF device.


### -field D3D10_DRIVER_TYPE_NULL

A NULL device; which is a reference device without render capability.


### -field D3D10_DRIVER_TYPE_SOFTWARE

Reserved for later use.


### -field D3D10_DRIVER_TYPE_WARP

A WARP driver, which is a high-performance software rasterizer. The rasterizer supports feature level 9_1 through level 10.1 with a 
        high performance software implementation when hardware is not available. For more information about using a WARP driver, see <a href="https://docs.microsoft.com/windows/desktop/direct3darticles/directx-warp">Windows Advanced Rasterization Platform (WARP) In-Depth Guide</a>.
        Note that WARP is only available with the DirectX 11 Runtime (Windows 7, Windows Server 2008 R2, updated Windows Vista [KB971644]).


## -remarks



The device-driver type needs to be specified when the device is created (using <a href="https://docs.microsoft.com/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice">D3D10CreateDevice</a> or <a href="https://docs.microsoft.com/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdeviceandswapchain">D3D10CreateDeviceAndSwapChain</a>). 

For information about limitations creating nonhardware-type devices on certain feature levels, see <a href="https://docs.microsoft.com/windows/desktop/direct3d11/overviews-direct3d-11-devices-limitations">Limitations Creating WARP and Reference Devices</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-enums">Core Enumerations</a>
 

 

