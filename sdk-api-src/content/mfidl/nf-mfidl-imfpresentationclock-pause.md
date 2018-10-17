---
UID: NF:mfidl.IMFPresentationClock.Pause
title: IMFPresentationClock::Pause
author: windows-sdk-content
description: Pauses the presentation clock. While the clock is paused, the clock time does not advance, and the clock's IMFPresentationClock::GetTime returns the time at which the clock was paused.
old-location: mf\imfpresentationclock_pause.htm
tech.root: medfound
ms.assetid: 2eddc9a9-e3a6-46c4-83c6-446b6a7a64b0
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: 2eddc9a9-e3a6-46c4-83c6-446b6a7a64b0, IMFPresentationClock interface [Media Foundation],Pause method, IMFPresentationClock.Pause, IMFPresentationClock::Pause, Pause, Pause method [Media Foundation], Pause method [Media Foundation],IMFPresentationClock interface, mf.imfpresentationclock_pause, mfidl/IMFPresentationClock::Pause
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IMFPresentationClock.Pause
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFPresentationClock::Pause


## -description



Pauses the presentation clock. While the clock is paused, the clock time does not advance, and the clock's <a href="https://msdn.microsoft.com/31037b75-9fa5-48e0-a58c-a451b445147f">IMFPresentationClock::GetTime</a> returns the time at which the clock was paused.




## -parameters






## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_CLOCK_NO_TIME_SOURCE</b></dt>
</dl>
</td>
<td width="60%">
No time source was set on this clock.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_CLOCK_STATE_ALREADY_SET</b></dt>
</dl>
</td>
<td width="60%">
The clock is already paused.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
The clock is stopped. This request is not valid when the clock is stopped.

</td>
</tr>
</table>
 




## -remarks



This method is valid when the clock is running. It is not valid when the clock is paused or stopped.

The presentation clock initiates the state change by calling <a href="https://msdn.microsoft.com/d4eb1ddf-2eea-48e2-946a-4ea20be8cc8f">IMFClockStateSink::OnClockPause</a> on the clock's time source. This call is made synchronously. If it fails, the state change does not occur. If the call succeeds, the state changes, and the clock notifies the other state-change subscribers by calling their <b>OnClockPause</b> methods. These calls are made asynchronously.




## -see-also




<a href="https://msdn.microsoft.com/979c4f77-cbee-468c-8f6b-e68442d89025">IMFPresentationClock</a>



<a href="https://msdn.microsoft.com/cb8bb62a-ef80-4de0-9a44-3bb77edc9dd5">Presentation Clock</a>
 

 

