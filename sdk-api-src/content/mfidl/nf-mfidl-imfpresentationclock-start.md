---
UID: NF:mfidl.IMFPresentationClock.Start
title: IMFPresentationClock::Start (mfidl.h)
description: Starts the presentation clock.
helpviewer_keywords: ["IMFPresentationClock interface [Media Foundation]","Start method","IMFPresentationClock.Start","IMFPresentationClock::Start","Start","Start method [Media Foundation]","Start method [Media Foundation]","IMFPresentationClock interface","ba5986d1-9c94-4747-a221-43d0583f1fed","mf.imfpresentationclock_start","mfidl/IMFPresentationClock::Start"]
old-location: mf\imfpresentationclock_start.htm
tech.root: mf
ms.assetid: ba5986d1-9c94-4747-a221-43d0583f1fed
ms.date: 12/05/2018
ms.keywords: IMFPresentationClock interface [Media Foundation],Start method, IMFPresentationClock.Start, IMFPresentationClock::Start, Start, Start method [Media Foundation], Start method [Media Foundation],IMFPresentationClock interface, ba5986d1-9c94-4747-a221-43d0583f1fed, mf.imfpresentationclock_start, mfidl/IMFPresentationClock::Start
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
 - IMFPresentationClock::Start
 - mfidl/IMFPresentationClock::Start
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
 - IMFPresentationClock.Start
---

# IMFPresentationClock::Start


## -description

Starts the presentation clock.

## -parameters

### -param llClockStartOffset [in]

Initial starting time, in 100-nanosecond units. At the time the <b>Start</b> method is called, the clock's <a href="/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime">IMFPresentationClock::GetTime</a> method returns this value, and the clock time increments from there. If the value is PRESENTATION_CURRENT_POSITION, the clock starts from its current position. Use this value if the clock is paused and you want to restart it from the same position.

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

If the clock is paused and restarted from the same position (<i>llClockStartOffset</i> is PRESENTATION_CURRENT_POSITION), the presentation clock sends an <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart">IMFClockStateSink::OnClockRestart</a> notification. Otherwise, the clock sends an <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart">IMFClockStateSink::OnClockStart</a> notification.

The presentation clock initiates the state change by calling <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart">OnClockStart</a> or <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart">OnClockRestart</a> on the clock's time source. This call is made synchronously. If it fails, the state change does not occur. If the call succeeds, the state changes, and the clock notifies the other state-change subscribers by calling their <b>OnClockStart</b> or <b>OnClockRestart</b> methods. These calls are made asynchronously.

If the clock is already running, calling <b>Start</b> again has the effect of seeking the clock to the new <i>StartOffset</i> position.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock">IMFPresentationClock</a>



<a href="/windows/desktop/medfound/presentation-clock">Presentation Clock</a>