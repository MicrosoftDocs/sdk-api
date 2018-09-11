---
UID: NN:mfidl.IMFPresentationClock
title: IMFPresentationClock
author: windows-sdk-content
description: Represents a presentation clock, which is used to schedule when samples are rendered and to synchronize multiple streams.
old-location: mf\imfpresentationclock.htm
tech.root: medfound
ms.assetid: 979c4f77-cbee-468c-8f6b-e68442d89025
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: 979c4f77-cbee-468c-8f6b-e68442d89025, IMFPresentationClock, IMFPresentationClock interface [Media Foundation], IMFPresentationClock interface [Media Foundation],described, mf.imfpresentationclock, mfidl/IMFPresentationClock
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
 - IMFPresentationClock
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFPresentationClock interface


## -description


Represents a presentation clock, which is used to schedule when samples are rendered and to synchronize multiple streams.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFPresentationClock</b> interface inherits from <a href="https://msdn.microsoft.com/3a60bfec-8511-4a84-a833-e0c73c593970">IMFClock</a>. <b>IMFPresentationClock</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/c90c3d26-51fa-4cd6-a154-6f72c21219d2">AddClockStateSink</a>
</td>
<td align="left" width="63%">
Registers an object to be notified whenever the clock starts, stops, or pauses, or changes rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/31037b75-9fa5-48e0-a58c-a451b445147f">GetTime</a>
</td>
<td align="left" width="63%">
Retrieves the latest clock time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6b6851b-f5b3-40c2-9160-59f2a68c9131">GetTimeSource</a>
</td>
<td align="left" width="63%">
Retrieves the clock's presentation time source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2eddc9a9-e3a6-46c4-83c6-446b6a7a64b0">Pause</a>
</td>
<td align="left" width="63%">
Pauses the presentation clock.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c037183d-a81f-4f49-9e02-06dc2476471f">RemoveClockStateSink</a>
</td>
<td align="left" width="63%">
Unregisters an object that is receiving state-change notifications from the clock.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/170b7c8e-9d1a-4168-964a-5fd057d1e8f9">SetTimeSource</a>
</td>
<td align="left" width="63%">
Sets the time source for the presentation clock.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ba5986d1-9c94-4747-a221-43d0583f1fed">Start</a>
</td>
<td align="left" width="63%">
Starts the presentation clock.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54377d65-2af7-410d-b8cf-45f467527a45">Stop</a>
</td>
<td align="left" width="63%">
Stops the presentation clock.

</td>
</tr>
</table> 


## -remarks



To create a new instance of the presentation clock, call the <a href="https://msdn.microsoft.com/b0ed3482-d127-45d3-a4de-271b1c0a199b">MFCreatePresentationClock</a> function. The presentation clock must have a time source, which is an object that provides the clock times. For example, the audio renderer is a time source that uses the sound card to drive the clock. Time sources expose the <a href="https://msdn.microsoft.com/e5fab6b7-0abc-4ad7-89a9-33c673e97ce2">IMFPresentationTimeSource</a> interface. To set the time source, call <a href="https://msdn.microsoft.com/170b7c8e-9d1a-4168-964a-5fd057d1e8f9">SetTimeSource</a>. The presentation clock does not begin running until the <a href="https://msdn.microsoft.com/ba5986d1-9c94-4747-a221-43d0583f1fed">Start</a> method is called.

To get the presentation clock from the Media Session, call <a href="https://msdn.microsoft.com/16444da2-68f2-4d94-8c6f-9e512d51e5e9">IMFMediaSession::GetClock</a>.




## -see-also




<a href="https://msdn.microsoft.com/3a60bfec-8511-4a84-a833-e0c73c593970">IMFClock</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/cb8bb62a-ef80-4de0-9a44-3bb77edc9dd5">Presentation Clock</a>
 

 

