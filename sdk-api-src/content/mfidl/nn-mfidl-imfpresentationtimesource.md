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

# IMFPresentationTimeSource interface


## -description



          Provides the clock times for the presentation clock.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFPresentationTimeSource</b> interface inherits from <a href="https://msdn.microsoft.com/3a60bfec-8511-4a84-a833-e0c73c593970">IMFClock</a>. <b>IMFPresentationTimeSource</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFPresentationTimeSource</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/09c8fef8-7288-4356-9671-4c927c0cf502">GetUnderlyingClock</a>
</td>
<td align="left" width="63%">
Retrieves the underlying clock that the presentation time source uses to generate its clock times.

</td>
</tr>
</table> 


## -remarks



This interface is implemented by presentation time sources. A presentation time source is an object that provides the clock time for the presentation clock. For example, the audio renderer is a presentation time source. The rate at which the audio renderer consumes audio samples determines the clock time. If the audio format is 44100 samples per second, the audio renderer will report that one second has passed for every 44100 audio samples it plays. In this case, the timing is provided by the sound card.

To set the presentation time source on the presentation clock, call <a href="https://msdn.microsoft.com/170b7c8e-9d1a-4168-964a-5fd057d1e8f9">IMFPresentationClock::SetTimeSource</a> with a pointer to the time source's <b>IMFPresentationTimeSource</b> interface.

A presentation time source must also implement the <a href="https://msdn.microsoft.com/9aa0d2cd-a687-4b3a-834d-ccc8d3a03196">IMFClockStateSink</a> interface. The presentaton clock uses this interface to notify the time source when the clock state changes.

Media Foundation provides a presentation time source that is based on the system clock. To create this object, call the <a href="https://msdn.microsoft.com/f3e7b8d5-fd6c-4d87-86f6-1117ca58bc6f">MFCreateSystemTimeSource</a> function.




## -see-also




<a href="https://msdn.microsoft.com/3a60bfec-8511-4a84-a833-e0c73c593970">IMFClock</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/cb8bb62a-ef80-4de0-9a44-3bb77edc9dd5">Presentation Clock</a>
 

 

