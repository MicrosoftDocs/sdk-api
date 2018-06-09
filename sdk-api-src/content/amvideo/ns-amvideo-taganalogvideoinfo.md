---
UID: NS:amvideo.tagAnalogVideoInfo
title: tagAnalogVideoInfo
author: windows-sdk-content
description: The ANALOGVIDEOINFO structure maintains information about the format of the analog video signal.
old-location: dshow\analogvideoinfo.htm
old-project: DirectShow
ms.assetid: c0c568ce-6834-4bfe-aaae-addfbc0218bd
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: ANALOGVIDEOINFO, ANALOGVIDEOINFO structure [DirectShow], ANALOGVIDEOINFOStructure, amvideo/ANALOGVIDEOINFO, dshow.analogvideoinfo, tagAnalogVideoInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: amvideo.h
req.include-header: Dshow.h
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
tech.root: 
req.typenames: ANALOGVIDEOINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - amvideo.h
api_name:
 - ANALOGVIDEOINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# tagAnalogVideoInfo structure


## -description



The <b>ANALOGVIDEOINFO</b> structure maintains information about the format of the analog video signal.




## -struct-fields




### -field rcSource

Source video rectangle.


### -field rcTarget

Destination target rectangle.


### -field dwActiveWidth

Source video width.


### -field dwActiveHeight

Source video height (483 for NTSC, 575 for PAL/SECAM).


### -field AvgTimePerFrame

Average time per frame in 100-nanosecond units.


## -remarks



Filters using this format usually pass the video signal using a hardware-based connection rather than using memory-based transports.

An example of a definition of an analog video media type connection would be a connection of NTSC video using "M" color encoding. This would use a major media type of MEDIATYPE_AnalogVideo, a subtype of MEDIASUBTYPE_AnalogVideo_NTSC_M, and a format type of FORMAT_AnalogVideo.




## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

