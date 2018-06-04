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
        high performance software implementation when hardware is not available. For more information about using a WARP driver, see <a href="https://msdn.microsoft.com/C40A96EB-64AA-46EB-85A9-7C996ABC8BFE">Windows Advanced Rasterization Platform (WARP) In-Depth Guide</a>.
        Note that WARP is only available with the DirectX 11 Runtime (Windows 7, Windows Server 2008 R2, updated Windows Vista [KB971644]).


## -remarks



The device-driver type needs to be specified when the device is created (using <a href="https://msdn.microsoft.com/da48d6d4-f35b-4cd1-a358-8eec63dfa674">D3D10CreateDevice</a> or <a href="https://msdn.microsoft.com/3123d45a-47ef-464f-9664-ba72f6688ce0">D3D10CreateDeviceAndSwapChain</a>). 

For information about limitations creating nonhardware-type devices on certain feature levels, see <a href="https://msdn.microsoft.com/7e022e5d-daa3-48fa-b9fe-4b569220e55e">Limitations Creating WARP and Reference Devices</a>.




## -see-also




<a href="https://msdn.microsoft.com/3d1541bf-75d8-459d-a912-4068e9a0a9e4">Core Enumerations</a>
 

 

