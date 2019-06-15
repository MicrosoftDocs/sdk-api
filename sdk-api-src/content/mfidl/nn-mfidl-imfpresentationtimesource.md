---
UID: NN:mfidl.IMFPresentationTimeSource
title: IMFPresentationTimeSource (mfidl.h)
author: windows-sdk-content
description: Provides the clock times for the presentation clock.
old-location: mf\imfpresentationtimesource.htm
tech.root: medfound
ms.assetid: e5fab6b7-0abc-4ad7-89a9-33c673e97ce2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFPresentationTimeSource, IMFPresentationTimeSource interface [Media Foundation], IMFPresentationTimeSource interface [Media Foundation],described, e5fab6b7-0abc-4ad7-89a9-33c673e97ce2, mf.imfpresentationtimesource, mfidl/IMFPresentationTimeSource
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFPresentationTimeSource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFPresentationTimeSource interface


## -description


Provides the clock times for the presentation clock.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFPresentationTimeSource</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfclock">IMFClock</a>. <b>IMFPresentationTimeSource</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfpresentationtimesource-getunderlyingclock">GetUnderlyingClock</a>
</td>
<td align="left" width="63%">
Retrieves the underlying clock that the presentation time source uses to generate its clock times.

</td>
</tr>
</table> 


## -remarks



This interface is implemented by presentation time sources. A presentation time source is an object that provides the clock time for the presentation clock. For example, the audio renderer is a presentation time source. The rate at which the audio renderer consumes audio samples determines the clock time. If the audio format is 44100 samples per second, the audio renderer will report that one second has passed for every 44100 audio samples it plays. In this case, the timing is provided by the sound card.

To set the presentation time source on the presentation clock, call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-settimesource">IMFPresentationClock::SetTimeSource</a> with a pointer to the time source's <b>IMFPresentationTimeSource</b> interface.

A presentation time source must also implement the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink">IMFClockStateSink</a> interface. The presentaton clock uses this interface to notify the time source when the clock state changes.

Media Foundation provides a presentation time source that is based on the system clock. To create this object, call the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-mfcreatesystemtimesource">MFCreateSystemTimeSource</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfclock">IMFClock</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/presentation-clock">Presentation Clock</a>
 

 

