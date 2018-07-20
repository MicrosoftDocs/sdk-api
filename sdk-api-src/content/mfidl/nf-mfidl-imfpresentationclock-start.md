---
UID: NF:mfidl.IMFPresentationClock.Start
title: IMFPresentationClock::Start
author: windows-sdk-content
description: Starts the presentation clock.
old-location: mf\imfpresentationclock_start.htm
old-project: medfound
ms.assetid: ba5986d1-9c94-4747-a221-43d0583f1fed
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IMFPresentationClock interface [Media Foundation],Start method, IMFPresentationClock.Start, IMFPresentationClock::Start, Start, Start method [Media Foundation], Start method [Media Foundation],IMFPresentationClock interface, ba5986d1-9c94-4747-a221-43d0583f1fed, mf.imfpresentationclock_start, mfidl/IMFPresentationClock::Start
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MFSensorDeviceMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFPresentationClock.Start
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFPresentationClock::Start


## -description



Starts the presentation clock.




## -parameters




### -param llClockStartOffset [in]

Initial starting time, in 100-nanosecond units. At the time the <b>Start</b> method is called, the clock's <a href="https://msdn.microsoft.com/31037b75-9fa5-48e0-a58c-a451b445147f">IMFPresentationClock::GetTime</a> method returns this value, and the clock time increments from there. If the value is PRESENTATION_CURRENT_POSITION, the clock starts from its current position. Use this value if the clock is paused and you want to restart it from the same position.


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
</table>
 




## -remarks



This method is valid in all states (stopped, paused, or running).

If the clock is paused and restarted from the same position (<i>llClockStartOffset</i> is PRESENTATION_CURRENT_POSITION), the presentation clock sends an <a href="https://msdn.microsoft.com/55973dfa-59b9-4105-9706-5d5497ad2818">IMFClockStateSink::OnClockRestart</a> notification. Otherwise, the clock sends an <a href="https://msdn.microsoft.com/1a696ffc-b8e6-4ef9-b980-35bfbd3d4128">IMFClockStateSink::OnClockStart</a> notification.

The presentation clock initiates the state change by calling <a href="https://msdn.microsoft.com/1a696ffc-b8e6-4ef9-b980-35bfbd3d4128">OnClockStart</a> or <a href="https://msdn.microsoft.com/55973dfa-59b9-4105-9706-5d5497ad2818">OnClockRestart</a> on the clock's time source. This call is made synchronously. If it fails, the state change does not occur. If the call succeeds, the state changes, and the clock notifies the other state-change subscribers by calling their <b>OnClockStart</b> or <b>OnClockRestart</b> methods. These calls are made asynchronously.

If the clock is already running, calling <b>Start</b> again has the effect of seeking the clock to the new <i>StartOffset</i> position.




## -see-also




<a href="https://msdn.microsoft.com/979c4f77-cbee-468c-8f6b-e68442d89025">IMFPresentationClock</a>



<a href="https://msdn.microsoft.com/cb8bb62a-ef80-4de0-9a44-3bb77edc9dd5">Presentation Clock</a>
 

 

