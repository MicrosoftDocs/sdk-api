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

# DrvIcmSetDeviceGammaRamp function


## -description


The <b>DrvIcmSetDeviceGammaRamp</b> function sets the hardware <a href="https://msdn.microsoft.com/f67c673d-c6f0-49f0-850a-d8b00e99ddd4">gamma ramp</a> of the specified display device.


## -parameters




### -param dhpdev

Handle to the physical device's <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">PDEV</a>. This identifies the physical device whose gamma ramp is to be set.


### -param iFormat

Specifies the data format of the buffer to which <i>lpRamp</i> points. This parameter is always IGRF_RGB_256WORDS.


### -param lpRamp

Pointer to the buffer containing the gamma ramp to be set on the device. The format of the data in this buffer is determined by <i>iFormat</i>.

When <i>iFormat</i> is IGRF_RGB_256WORDS, <i>lpRamp</i> points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff566479">GAMMARAMP</a> structure that defines the 256-entry ramps to be set for each of the red, blue, and green color channels. Each value is described using 16-bit precision. If the hardware has fewer bits of precision, it should downshift and use the most significant bits, without rounding.


## -returns



<b>DrvIcmSetDeviceGammaRamp</b> returns <b>TRUE</b> upon success. Otherwise, it returns <b>FALSE</b>.




## -remarks



Drivers for display devices with loadable hardware gamma ramps should implement this function.

<b>DrvIcmSetDeviceGammaRamp</b> should fail if it is called with any other value besides IGRF_RGB_256WORDS in <i>iFormat</i>.

The driver hooks this function by setting the GCAPS2_CHANGEGAMMARAMP flag in the <b>flGraphicsCaps2</b> field of the DEVINFO structure passed to <a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a>. If the driver is running in a palettized 8bpp mode, this capability is optional. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a>
 

 

