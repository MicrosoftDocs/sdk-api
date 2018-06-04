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

# _BP_BUFFERFORMAT enumeration


## -description


Specifies the format of the buffer. Used by <a href="https://msdn.microsoft.com/ca7204b3-3166-4911-96f9-16a0f59ecb09">BeginBufferedAnimation</a> and <a href="https://msdn.microsoft.com/da574e22-b08e-47e8-b874-e158862c2f9a">BeginBufferedPaint</a>.


## -enum-fields




### -field BPBF_COMPATIBLEBITMAP

Compatible bitmap. The  number of bits per pixel is based on the color format of the device associated with the HDC specified with <a href="https://msdn.microsoft.com/da574e22-b08e-47e8-b874-e158862c2f9a">BeginBufferedPaint</a> or <a href="https://msdn.microsoft.com/ca7204b3-3166-4911-96f9-16a0f59ecb09">BeginBufferedAnimation</a>—typically, this is the display device.


### -field BPBF_DIB

Bottom-up device-independent bitmap. The origin of the bitmap is the lower-left corner. Uses 32 bits per pixel.


### -field BPBF_TOPDOWNDIB

Top-down device-independent bitmap. The origin of the bitmap is the upper-left corner. Uses 32 bits per pixel.


### -field BPBF_TOPDOWNMONODIB

Top-down, monochrome, device-independent bitmap. Uses 1 bit per pixel.


## -see-also




<a href="https://msdn.microsoft.com/d2866beb-ff7a-4390-8651-e7bf458ddf88">CreateCompatibleBitmap</a>



<a href="https://msdn.microsoft.com/56b39a3d-48a4-4620-9652-ec41ea4d6423">Device-Independent Bitmaps</a>



<b>Other Resources</b>
 

 

