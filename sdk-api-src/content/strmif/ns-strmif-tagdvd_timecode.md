---
UID: NS:strmif.tagDVD_TIMECODE
title: tagDVD_TIMECODE
author: windows-sdk-content
description: The DVD_TIMECODE structure contains DVD timecode in hours, minutes, seconds, and frames.
old-location: dshow\dvd_timecode.htm
old-project: DirectShow
ms.assetid: 7ad0b11e-5bb7-426f-9a2c-fbc34b2f45b4
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: DVD_TIMECODE, DVD_TIMECODE structure [DirectShow], DVD_TIMECODEStructure, dshow.dvd_timecode, strmif/DVD_TIMECODE, tagDVD_TIMECODE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: strmif.h
req.include-header: Dshow.h
req.redist: 
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
req.typenames: DVD_TIMECODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - DVD_TIMECODE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# tagDVD_TIMECODE structure


## -description



The <code>DVD_TIMECODE</code> structure contains DVD timecode in hours, minutes, seconds, and frames.




## -struct-fields




### -field Hours1

Hours.


### -field Hours10

Tens of hours.


### -field Minutes1

Minutes.


### -field Minutes10

Tens of minutes.


### -field Seconds1

Seconds.


### -field Seconds10

Tens of seconds.


### -field Frames1

Frames.


### -field Frames10

Tens of frames.


### -field FrameRateCode

Frames per second dropped and not dropped as indicated by <a href="https://msdn.microsoft.com/92309c56-87fe-43cc-b76e-43f9686177be">DVD_FRAMERATE</a>.


## -remarks



DVD timecode is binary coded decimal (BCD) encoded in the format 0xHhMmSsFf, where:

<ul>
<li>H is tens of hours</li>
<li>h is hours</li>
<li>M is tens of minutes</li>
<li>m is minutes</li>
<li>S is tens of seconds</li>
<li>s is seconds</li>
<li>F is tens of frames</li>
<li>f is frames</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

