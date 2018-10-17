---
UID: NN:mfidl.IMFClockStateSink
title: IMFClockStateSink
author: windows-sdk-content
description: Receives state-change notifications from the presentation clock.
old-location: mf\imfclockstatesink.htm
tech.root: medfound
ms.assetid: 9aa0d2cd-a687-4b3a-834d-ccc8d3a03196
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: 9aa0d2cd-a687-4b3a-834d-ccc8d3a03196, IMFClockStateSink, IMFClockStateSink interface [Media Foundation], IMFClockStateSink interface [Media Foundation],described, mf.imfclockstatesink, mfidl/IMFClockStateSink
ms.prod: windows
ms.technology: windows-sdk
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
---

# IMFClockStateSink interface


## -description


Receives state-change notifications from the presentation clock.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFClockStateSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFClockStateSink</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/d4eb1ddf-2eea-48e2-946a-4ea20be8cc8f">OnClockPause</a>
</td>
<td align="left" width="63%">
Called when the presentation clock pauses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/55973dfa-59b9-4105-9706-5d5497ad2818">OnClockRestart</a>
</td>
<td align="left" width="63%">
Called when the presentation clock restarts from the same position while paused.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ba8afdf9-13eb-4e3d-b8a7-c74e0b40e998">OnClockSetRate</a>
</td>
<td align="left" width="63%">
Called when the rate changes on the presentation clock.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a696ffc-b8e6-4ef9-b980-35bfbd3d4128">OnClockStart</a>
</td>
<td align="left" width="63%">
Called when the presentation clock starts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/472b704f-d402-4e0b-96b8-fea267e8ff63">OnClockStop</a>
</td>
<td align="left" width="63%">
Called when the presentation clock stops.

</td>
</tr>
</table> 


## -remarks



To receive state-change notifications from the presentation clock, implement this interface and call <a href="https://msdn.microsoft.com/c90c3d26-51fa-4cd6-a154-6f72c21219d2">IMFPresentationClock::AddClockStateSink</a> on the presentation clock.

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




<a href="https://msdn.microsoft.com/e5fab6b7-0abc-4ad7-89a9-33c673e97ce2">IMFPresentationTimeSource</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/cb8bb62a-ef80-4de0-9a44-3bb77edc9dd5">Presentation Clock</a>
 

 

