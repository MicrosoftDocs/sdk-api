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

# tagWMVIDEOINFOHEADER structure


## -description



The <b>WMVIDEOINFOHEADER</b> structure describes the bitmap and color information for a video image.




## -struct-fields




### -field rcSource

<b>RECT</b> structure that specifies the source video window.


### -field rcTarget

<b>RECT</b> structure that specifies the destination video window.


### -field dwBitRate

<b>DWORD</b> containing the approximate bit rate, in bits per second.


### -field dwBitErrorRate

<b>DWORD</b> containing the error rate for this stream, in bits per second.


### -field AvgTimePerFrame

When writing an ASF file, this member specifies the desired average time per frame in 100-nanosecond units. When reading an ASF file, this member is always zero.


### -field bmiHeader

<b>BITMAPINFOHEADER</b> structure that contains color and dimension information for the video image bitmap. <b>BITMAPINFOHEADER</b> is a Windows GDI structure.


## -remarks



This structure is identical to the DirectShow <b>VIDEOINFOHEADER</b> structure.

For uncompressed video of 16 or fewer bits per pixel (bpp), additional information is required. You must specify bit fields for 16 bpp and palette information for 8 or fewer bpp video. To convey this information, allocate enough consecutive memory to hold the additional information and copy the data to the memory directly following this structure. When you specify the address and size of this structure in the <a href="https://msdn.microsoft.com/37a9ac59-e152-47e1-96ee-b816cd645936">WM_MEDIA_TYPE</a> structure for a stream, include the size of the palette or bit field data.



