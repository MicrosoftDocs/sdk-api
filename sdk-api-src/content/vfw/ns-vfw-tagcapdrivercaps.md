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

# tagCapDriverCaps structure


## -description



The <b>CAPDRIVERCAPS</b> structure defines the capabilities of the capture driver.

An application should use the <a href="https://msdn.microsoft.com/898a800c-1109-47cd-bcc9-cb61d86a4a2e">WM_CAP_DRIVER_GET_CAPS</a> message or <a href="https://msdn.microsoft.com/2ca3a1b1-1d88-480f-b079-82da111c4565">capDriverGetCaps</a> macro to place a copy of the driver capabilities in a <b>CAPDRIVERCAPS</b> structure whenever the application connects a capture window to a capture driver.




## -struct-fields




### -field wDeviceIndex

Index of the capture driver. An index value can range from 0 to 9.


### -field fHasOverlay

Video-overlay flag. The value of this member is <b>TRUE</b> if the device supports video overlay.


### -field fHasDlgVideoSource

Video source dialog flag. The value of this member is <b>TRUE</b> if the device supports a dialog box for selecting and controlling the video source.


### -field fHasDlgVideoFormat

Video format dialog flag. The value of this member is <b>TRUE</b> if the device supports a dialog box for selecting the video format.


### -field fHasDlgVideoDisplay

Video display dialog flag. The value of this member is <b>TRUE</b> if the device supports a dialog box for controlling the redisplay of video from the capture frame buffer.


### -field fCaptureInitialized

Capture initialization flag. The value of this member is <b>TRUE</b> if a capture device has been successfully connected.


### -field fDriverSuppliesPalettes

Driver palette flag. The value of this member is <b>TRUE</b> if the driver can create palettes.


### -field hVideoIn

Not used in Win32 applications.


### -field hVideoOut

Not used in Win32 applications.


### -field hVideoExtIn

Not used in Win32 applications.


### -field hVideoExtOut

Not used in Win32 applications.


## -see-also




Video Capture



<a href="https://msdn.microsoft.com/180010d2-240e-433d-b306-341b9b1e0b57">Video Capture Structures</a>
 

 

