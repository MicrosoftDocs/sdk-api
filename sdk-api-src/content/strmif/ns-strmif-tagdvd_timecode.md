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
 

 

