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

# tagWMVIDEOINFOHEADER2 structure


## -description



The <b>WMVIDEOINFOHEADER2</b> structure describes the bitmap and color information for a video image, including <a href="wmformat_glossary.htm">interlace</a>, copy protection, and aspect ratio.




## -struct-fields




### -field rcSource

<b>RECT</b> structure that specifies what part of the source stream should be used to fill the destination buffer. Renderers can use this field to ask the decoders to stretch or clip.


### -field rcTarget

<b>RECT</b> structure that specifies that specifies what part of the destination buffer should be used


### -field dwBitRate

Approximate data rate of the video stream, in bits per second.


### -field dwBitErrorRate

Data error rate of the video stream, in bits per second.


### -field AvgTimePerFrame

The video frame's average display time, in 100-nanosecond units.


### -field dwInterlaceFlags

Bit-wise combination of zero or more flags that describe interlacing behavior. The flags are defined in Dvdmedia.h in the DirectX SDK. Undefined bits must be set to zero or else the connection will be rejected.


### -field dwCopyProtectFlags

Flag set with the AMCOPYPROTECT_RestrictDuplication value (0x00000001) to indicate that the duplication of the stream should be restricted. Undefined bits must be set to zero or else the connection will be rejected.


### -field dwPictAspectRatioX

The X dimension of the video rectangle's aspect ratio. For example, 16 for a 16:9 rectangle.


### -field dwPictAspectRatioY

The Y dimension of the video rectangle's aspect ratio. For example, 9 for a 16:9 rectangle.


### -field dwReserved1

Reserved for future use. Must be zero. (Note: this is different from the corresponding member of the <b>VIDEOINFOHEADER2</b> structure used in DirectShow.


### -field dwReserved2

Reserved for future use. Must be zero.


### -field bmiHeader

<b>BITMAPINFOHEADER</b> structure that contains color and dimension information for the video image bitmap.


## -remarks



This structure is identical to the <b>VIDEOINFOHEADER2</b> structure defined in Dvdmedia.h. For more information, see the DirectShow documentation in the DirectX SDK.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

