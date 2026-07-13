---
UID: NF:mfidl.IMFMediaSink.SetPresentationClock
title: IMFMediaSink::SetPresentationClock (mfidl.h)
description: Sets the presentation clock on the media sink.
helpviewer_keywords: ["844fc3b3-b56e-4048-b589-e24457bcc419","IMFMediaSink interface [Media Foundation]","SetPresentationClock method","IMFMediaSink.SetPresentationClock","IMFMediaSink::SetPresentationClock","SetPresentationClock","SetPresentationClock method [Media Foundation]","SetPresentationClock method [Media Foundation]","IMFMediaSink interface","mf.imfmediasink_setpresentationclock","mfidl/IMFMediaSink::SetPresentationClock"]
old-location: mf\imfmediasink_setpresentationclock.htm
tech.root: mf
ms.assetid: 844fc3b3-b56e-4048-b589-e24457bcc419
ms.date: 12/05/2018
ms.keywords: 844fc3b3-b56e-4048-b589-e24457bcc419, IMFMediaSink interface [Media Foundation],SetPresentationClock method, IMFMediaSink.SetPresentationClock, IMFMediaSink::SetPresentationClock, SetPresentationClock, SetPresentationClock method [Media Foundation], SetPresentationClock method [Media Foundation],IMFMediaSink interface, mf.imfmediasink_setpresentationclock, mfidl/IMFMediaSink::SetPresentationClock
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
 - IMFMediaSink::SetPresentationClock
 - mfidl/IMFMediaSink::SetPresentationClock
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
 - IMFMediaSink.SetPresentationClock
---

# IMFMediaSink::SetPresentationClock


## -description

Sets the presentation clock on the media sink.

## -parameters

### -param pPresentationClock [in]

Pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock">IMFPresentationClock</a> interface of the presentation clock, or <b>NULL</b>. If the value is <b>NULL</b>, the media sink stops listening to the presentation clock that was previously set, if any.

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
The presentation clock does not have a time source. Call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-settimesource">SetTimeSource</a> on the presentation clock.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The media sink's <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-shutdown">Shutdown</a> method has been called.

</td>
</tr>
</table>

## -remarks

During streaming, the media sink attempts to match rates with the presentation clock. Ideally, the media sink presents samples at the correct time according to the presentation clock and does not fall behind. Rateless media sinks are an exception to this rule, as they consume samples as quickly as possible and ignore the clock. If the sink is rateless, the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics">IMFMediaSink::GetCharacteristics</a> method returns the MEDIASINK_RATELESS flag.

The presentation clock must have a time source. Before calling this method, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-settimesource">IMFPresentationClock::SetTimeSource</a> on the presentation clock to set the presentation time source. Some media sinks provide time sources; therefore, the media sink might be the time source for its own presentation clock. Regardless of what object provides the time source, however, the media sink must attempt to match rates with the clock specified in <i>pPresentationClock</i>. If a media sink cannot match rates with an external time source, the media sink's <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics">IMFMediaSink::GetCharacteristics</a> method retrieves the MEDIASINK_CANNOT_MATCH_CLOCK flag. In this case, <b>SetPresentationClock</b> will still succeed, but the results will not be optimal. The sink might not render samples quickly enough to match rates with the presentation clock.

If <i>pPresentationClock</i> is non-<b>NULL</b>, the media sink must register for clock state notifications, by calling <a href="/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-addclockstatesink">IMFPresentationClock::AddClockStateSink</a> on the presentation clock. If the method is called again with a new presentation clock, or if <i>pPresentationClock</i> is <b>NULL</b>, the media sink must call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-removeclockstatesink">IMFPresentationClock::RemoveClockStateSink</a> to deregister itself from the previous clock.

All media sinks must support this method.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasink">IMFMediaSink</a>



<a href="/windows/desktop/medfound/media-sinks">Media Sinks</a>



<a href="/windows/desktop/medfound/presentation-clock">Presentation Clock</a>