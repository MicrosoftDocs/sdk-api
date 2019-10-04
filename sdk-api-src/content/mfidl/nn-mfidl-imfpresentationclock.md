---
UID: NN:mfidl.IMFPresentationClock
title: IMFPresentationClock (mfidl.h)
author: windows-sdk-content
description: Represents a presentation clock, which is used to schedule when samples are rendered and to synchronize multiple streams.
old-location: mf\imfpresentationclock.htm
tech.root: medfound
ms.assetid: 979c4f77-cbee-468c-8f6b-e68442d89025
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 979c4f77-cbee-468c-8f6b-e68442d89025, IMFPresentationClock, IMFPresentationClock interface [Media Foundation], IMFPresentationClock interface [Media Foundation],described, mf.imfpresentationclock, mfidl/IMFPresentationClock
ms.topic: interface
f1_keywords: 
 - "mfidl/IMFPresentationClock"
dev_langs:
 - c++
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
 - IMFPresentationClock
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFPresentationClock interface


## -description


Represents a presentation clock, which is used to schedule when samples are rendered and to synchronize multiple streams.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFPresentationClock</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfclock">IMFClock</a>. <b>IMFPresentationClock</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFPresentationClock</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-addclockstatesink">AddClockStateSink</a>
</td>
<td align="left" width="63%">
Registers an object to be notified whenever the clock starts, stops, or pauses, or changes rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime">GetTime</a>
</td>
<td align="left" width="63%">
Retrieves the latest clock time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettimesource">GetTimeSource</a>
</td>
<td align="left" width="63%">
Retrieves the clock's presentation time source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-pause">Pause</a>
</td>
<td align="left" width="63%">
Pauses the presentation clock.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-removeclockstatesink">RemoveClockStateSink</a>
</td>
<td align="left" width="63%">
Unregisters an object that is receiving state-change notifications from the clock.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-settimesource">SetTimeSource</a>
</td>
<td align="left" width="63%">
Sets the time source for the presentation clock.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-start">Start</a>
</td>
<td align="left" width="63%">
Starts the presentation clock.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-stop">Stop</a>
</td>
<td align="left" width="63%">
Stops the presentation clock.

</td>
</tr>
</table> 


## -remarks



To create a new instance of the presentation clock, call the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationclock">MFCreatePresentationClock</a> function. The presentation clock must have a time source, which is an object that provides the clock times. For example, the audio renderer is a time source that uses the sound card to drive the clock. Time sources expose the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource">IMFPresentationTimeSource</a> interface. To set the time source, call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-settimesource">SetTimeSource</a>. The presentation clock does not begin running until the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-start">Start</a> method is called.

To get the presentation clock from the Media Session, call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock">IMFMediaSession::GetClock</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfclock">IMFClock</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/presentation-clock">Presentation Clock</a>
 

 

