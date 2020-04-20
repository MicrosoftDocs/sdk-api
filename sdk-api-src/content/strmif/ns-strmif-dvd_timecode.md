---
UID: NS:strmif.tagDVD_TIMECODE
title: DVD_TIMECODE (strmif.h)
description: The DVD_TIMECODE structure contains DVD timecode in hours, minutes, seconds, and frames.helpviewer_keywords: ["DVD_TIMECODE","DVD_TIMECODE structure [DirectShow]","DVD_TIMECODEStructure","dshow.dvd_timecode","strmif/DVD_TIMECODE"]
old-location: dshow\dvd_timecode.htm
tech.root: DirectShow
ms.assetid: 7ad0b11e-5bb7-426f-9a2c-fbc34b2f45b4
ms.date: 12/05/2018
ms.keywords: DVD_TIMECODE, DVD_TIMECODE structure [DirectShow], DVD_TIMECODEStructure, dshow.dvd_timecode, strmif/DVD_TIMECODE
f1_keywords:
- strmif/DVD_TIMECODE
dev_langs:
- c++
req.header: strmif.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- strmif.h
api_name:
- DVD_TIMECODE
targetos: Windows
req.typenames: DVD_TIMECODE
req.redist: 
ms.custom: 19H1
---

# DVD_TIMECODE structure


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

Frames per second dropped and not dropped as indicated by [DVD_FRAMERATE](https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-dvd_framerate).


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




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>
 

 

