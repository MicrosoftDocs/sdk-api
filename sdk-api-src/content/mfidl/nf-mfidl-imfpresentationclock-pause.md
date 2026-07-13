---
UID: NF:mfidl.IMFPresentationClock.Pause
title: IMFPresentationClock::Pause (mfidl.h)
description: Pauses the presentation clock. While the clock is paused, the clock time does not advance, and the clock's IMFPresentationClock::GetTime returns the time at which the clock was paused.
helpviewer_keywords: ["2eddc9a9-e3a6-46c4-83c6-446b6a7a64b0","IMFPresentationClock interface [Media Foundation]","Pause method","IMFPresentationClock.Pause","IMFPresentationClock::Pause","Pause","Pause method [Media Foundation]","Pause method [Media Foundation]","IMFPresentationClock interface","mf.imfpresentationclock_pause","mfidl/IMFPresentationClock::Pause"]
old-location: mf\imfpresentationclock_pause.htm
tech.root: mf
ms.assetid: 2eddc9a9-e3a6-46c4-83c6-446b6a7a64b0
ms.date: 12/05/2018
ms.keywords: 2eddc9a9-e3a6-46c4-83c6-446b6a7a64b0, IMFPresentationClock interface [Media Foundation],Pause method, IMFPresentationClock.Pause, IMFPresentationClock::Pause, Pause, Pause method [Media Foundation], Pause method [Media Foundation],IMFPresentationClock interface, mf.imfpresentationclock_pause, mfidl/IMFPresentationClock::Pause
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
 - IMFPresentationClock::Pause
 - mfidl/IMFPresentationClock::Pause
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
 - IMFPresentationClock.Pause
---

# IMFPresentationClock::Pause


## -description

Pauses the presentation clock. While the clock is paused, the clock time does not advance, and the clock's <a href="/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime">IMFPresentationClock::GetTime</a> returns the time at which the clock was paused.



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

The presentation clock initiates the state change by calling <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockpause">IMFClockStateSink::OnClockPause</a> on the clock's time source. This call is made synchronously. If it fails, the state change does not occur. If the call succeeds, the state changes, and the clock notifies the other state-change subscribers by calling their <b>OnClockPause</b> methods. These calls are made asynchronously.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock">IMFPresentationClock</a>



<a href="/windows/desktop/medfound/presentation-clock">Presentation Clock</a>
