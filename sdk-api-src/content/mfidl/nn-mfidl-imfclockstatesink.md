---
UID: NN:mfidl.IMFClockStateSink
title: IMFClockStateSink (mfidl.h)
author: windows-sdk-content
description: Receives state-change notifications from the presentation clock.
old-location: mf\imfclockstatesink.htm
tech.root: medfound
ms.assetid: 9aa0d2cd-a687-4b3a-834d-ccc8d3a03196
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 9aa0d2cd-a687-4b3a-834d-ccc8d3a03196, IMFClockStateSink, IMFClockStateSink interface [Media Foundation], IMFClockStateSink interface [Media Foundation],described, mf.imfclockstatesink, mfidl/IMFClockStateSink
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
 - IMFClockStateSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFClockStateSink interface


## -description


Receives state-change notifications from the presentation clock.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFClockStateSink</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFClockStateSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFClockStateSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockpause">OnClockPause</a>
</td>
<td align="left" width="63%">
Called when the presentation clock pauses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart">OnClockRestart</a>
</td>
<td align="left" width="63%">
Called when the presentation clock restarts from the same position while paused.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate">OnClockSetRate</a>
</td>
<td align="left" width="63%">
Called when the rate changes on the presentation clock.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart">OnClockStart</a>
</td>
<td align="left" width="63%">
Called when the presentation clock starts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop">OnClockStop</a>
</td>
<td align="left" width="63%">
Called when the presentation clock stops.

</td>
</tr>
</table> 


## -remarks



To receive state-change notifications from the presentation clock, implement this interface and call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-addclockstatesink">IMFPresentationClock::AddClockStateSink</a> on the presentation clock.

This interface must be implemented by:

<ul>
<li>
Presentation time sources. The presentation clock uses this interface to request change states from the time source.

</li>
<li>
Media sinks. Media sinks use this interface to get notifications when the presentation clock changes.

</li>
</ul>
Other objects that need to be notified can implement this interface.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource">IMFPresentationTimeSource</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/presentation-clock">Presentation Clock</a>
 

 

