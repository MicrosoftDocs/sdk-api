---
UID: NF:mfidl.IMFPresentationClock.Stop
title: IMFPresentationClock::Stop
author: windows-sdk-content
description: Stops the presentation clock. While the clock is stopped, the clock time does not advance, and the clock's IMFPresentationClock::GetTime method returns zero.
old-location: mf\imfpresentationclock_stop.htm
tech.root: medfound
ms.assetid: 54377d65-2af7-410d-b8cf-45f467527a45
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 54377d65-2af7-410d-b8cf-45f467527a45, IMFPresentationClock interface [Media Foundation],Stop method, IMFPresentationClock.Stop, IMFPresentationClock::Stop, Stop, Stop method [Media Foundation], Stop method [Media Foundation],IMFPresentationClock interface, mf.imfpresentationclock_stop, mfidl/IMFPresentationClock::Stop
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
 - IMFPresentationClock.Stop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFPresentationClock::Stop


## -description



Stops the presentation clock. While the clock is stopped, the clock time does not advance, and the clock's <a href="https://msdn.microsoft.com/31037b75-9fa5-48e0-a58c-a451b445147f">IMFPresentationClock::GetTime</a> method returns zero.




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
The clock is already stopped.

</td>
</tr>
</table>
 




## -remarks



This method is valid when the clock is running or paused.

The presentation clock initiates the state change by calling <a href="https://msdn.microsoft.com/472b704f-d402-4e0b-96b8-fea267e8ff63">IMFClockStateSink::OnClockStop</a> on the clock's time source. This call is made synchronously. If it fails, the state change does not occur. If the call succeeds, the state changes, and the clock notifies the other state-change subscribers by calling their <b>OnClockStop</b> methods. These calls are made asynchronously.




## -see-also




<a href="https://msdn.microsoft.com/979c4f77-cbee-468c-8f6b-e68442d89025">IMFPresentationClock</a>



<a href="https://msdn.microsoft.com/cb8bb62a-ef80-4de0-9a44-3bb77edc9dd5">Presentation Clock</a>
 

 

