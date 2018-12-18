---
UID: NF:winddi.DrvIcmSetDeviceGammaRamp
title: DrvIcmSetDeviceGammaRamp function
author: windows-sdk-content
description: The DrvIcmSetDeviceGammaRamp function sets the hardware gamma ramp of the specified display device.
old-location: display\drvicmsetdevicegammaramp.htm
tech.root: display
ms.assetid: 0ea0c60c-fa12-4dd0-a6cc-45eacf4b73c0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DrvIcmSetDeviceGammaRamp, DrvIcmSetDeviceGammaRamp function [Display Devices], ddifncs_4f81d949-51a0-4d83-b779-e9e950c2851d.xml, display.drvicmsetdevicegammaramp, winddi/DrvIcmSetDeviceGammaRamp
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Desktop
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
 - winddi.h
api_name:
 - DrvIcmSetDeviceGammaRamp
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

When <i>iFormat</i> is IGRF_RGB_256WORDS, <i>lpRamp</i> points to a <a href="https://msdn.microsoft.com/cc082911-5089-4335-93d2-1405ca390741">GAMMARAMP</a> structure that defines the 256-entry ramps to be set for each of the red, blue, and green color channels. Each value is described using 16-bit precision. If the hardware has fewer bits of precision, it should downshift and use the most significant bits, without rounding.


## -returns



<b>DrvIcmSetDeviceGammaRamp</b> returns <b>TRUE</b> upon success. Otherwise, it returns <b>FALSE</b>.




## -remarks



Drivers for display devices with loadable hardware gamma ramps should implement this function.

<b>DrvIcmSetDeviceGammaRamp</b> should fail if it is called with any other value besides IGRF_RGB_256WORDS in <i>iFormat</i>.

The driver hooks this function by setting the GCAPS2_CHANGEGAMMARAMP flag in the <b>flGraphicsCaps2</b> field of the DEVINFO structure passed to <a href="https://msdn.microsoft.com/9a7ed18a-f21c-486b-9261-59a3fe5aef9e">DrvEnablePDEV</a>. If the driver is running in a palettized 8bpp mode, this capability is optional. 




## -see-also




<a href="https://msdn.microsoft.com/9a7ed18a-f21c-486b-9261-59a3fe5aef9e">DrvEnablePDEV</a>
 

 

