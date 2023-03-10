---
UID: NF:mfidl.IMFPresentationClock.Stop
title: IMFPresentationClock::Stop (mfidl.h)
description: Stops the presentation clock. While the clock is stopped, the clock time does not advance, and the clock's IMFPresentationClock::GetTime method returns zero.
helpviewer_keywords: ["54377d65-2af7-410d-b8cf-45f467527a45","IMFPresentationClock interface [Media Foundation]","Stop method","IMFPresentationClock.Stop","IMFPresentationClock::Stop","Stop","Stop method [Media Foundation]","Stop method [Media Foundation]","IMFPresentationClock interface","mf.imfpresentationclock_stop","mfidl/IMFPresentationClock::Stop"]
old-location: mf\imfpresentationclock_stop.htm
tech.root: mf
ms.assetid: 54377d65-2af7-410d-b8cf-45f467527a45
ms.date: 12/05/2018
ms.keywords: 54377d65-2af7-410d-b8cf-45f467527a45, IMFPresentationClock interface [Media Foundation],Stop method, IMFPresentationClock.Stop, IMFPresentationClock::Stop, Stop, Stop method [Media Foundation], Stop method [Media Foundation],IMFPresentationClock interface, mf.imfpresentationclock_stop, mfidl/IMFPresentationClock::Stop
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFPresentationClock::Stop
 - mfidl/IMFPresentationClock::Stop
dev_langs:
 - c++
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
---

# IMFPresentationClock::Stop


## -description

Stops the presentation clock. While the clock is stopped, the clock time does not advance, and the clock's <a href="/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime">IMFPresentationClock::GetTime</a> method returns zero.



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

The presentation clock initiates the state change by calling <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop">IMFClockStateSink::OnClockStop</a> on the clock's time source. This call is made synchronously. If it fails, the state change does not occur. If the call succeeds, the state changes, and the clock notifies the other state-change subscribers by calling their <b>OnClockStop</b> methods. These calls are made asynchronously.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock">IMFPresentationClock</a>



<a href="/windows/desktop/medfound/presentation-clock">Presentation Clock</a>
