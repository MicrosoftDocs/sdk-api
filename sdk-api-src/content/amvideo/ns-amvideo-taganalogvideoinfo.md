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
 

 

