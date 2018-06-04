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

# _AMVPDATAINFO structure


## -description



The <b>AMVPDATAINFO</b> structure specifies the data-specific characteristics of the VP input stream.




## -struct-fields




### -field dwSize

Size of the structure, in bytes.


### -field dwMicrosecondsPerField

Time taken by each field.


### -field amvpDimInfo

Dimensional information.


### -field dwPictAspectRatioX

The X dimension of picture aspect ratio.


### -field dwPictAspectRatioY

The Y dimension of picture aspect ratio.


### -field bEnableDoubleClock

Video port should enable double clocking.


### -field bEnableVACT

Video port should use an external VACT signal.


### -field bDataIsInterlaced

Indicates that the signal is interlaced.


### -field lHalfLinesOdd

Number of half lines in the odd field.


### -field bFieldPolarityInverted

Video port should invert the field polarity.


### -field dwNumLinesInVREF

Number of lines of data in VREF.


### -field lHalfLinesEven

Number of half lines in the even field.


### -field dwReserved1

Reserved for future use.


## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

