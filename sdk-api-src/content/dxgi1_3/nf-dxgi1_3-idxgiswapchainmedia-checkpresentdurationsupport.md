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

# IDXGISwapChainMedia::CheckPresentDurationSupport


## -description


Queries the graphics driver for a supported frame present duration corresponding to a custom refresh rate.


## -parameters




### -param DesiredPresentDuration

Indicates the frame duration to check. This value is the duration of one frame at the desired refresh rate, specified in hundreds of nanoseconds. For example, set this field to 167777 to check for 60 Hz refresh rate support.


### -param pClosestSmallerPresentDuration [out]

A variable that will be set to the closest supported frame present duration that's smaller than the requested value, or zero if the device does not support any lower duration.


### -param pClosestLargerPresentDuration [out]

A variable that will be set to the closest supported frame present duration that's larger than the requested value, or zero if the device does not support any higher duration.


## -returns



This method returns S_OK on success, or a DXGI error code on failure.




## -remarks



If the DXGI output adapter does not support custom refresh rates (for example, an external display) then the display driver will set upper and lower bounds to (0, 0).




## -see-also




<a href="https://msdn.microsoft.com/80C2A6D8-3435-4671-A473-0EF0F5A70ADB">IDXGISwapChainMedia</a>
 

 

