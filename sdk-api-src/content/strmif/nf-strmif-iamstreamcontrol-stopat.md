---
UID: NF:strmif.IAMStreamControl.StopAt
title: IAMStreamControl::StopAt (strmif.h)
description: The StopAt method informs the pin when to stop delivering data.
helpviewer_keywords: ["IAMStreamControl interface [DirectShow]","StopAt method","IAMStreamControl.StopAt","IAMStreamControl::StopAt","IAMStreamControlStopAt","StopAt","StopAt method [DirectShow]","StopAt method [DirectShow]","IAMStreamControl interface","dshow.iamstreamcontrol_stopat","strmif/IAMStreamControl::StopAt"]
old-location: dshow\iamstreamcontrol_stopat.htm
tech.root: dshow
ms.assetid: b3dd5332-e93e-4e55-9c7f-47c302ef11a3
ms.date: 4/26/2023
ms.keywords: IAMStreamControl interface [DirectShow],StopAt method, IAMStreamControl.StopAt, IAMStreamControl::StopAt, IAMStreamControlStopAt, StopAt, StopAt method [DirectShow], StopAt method [DirectShow],IAMStreamControl interface, dshow.iamstreamcontrol_stopat, strmif/IAMStreamControl::StopAt
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMStreamControl::StopAt
 - strmif/IAMStreamControl::StopAt
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMStreamControl.StopAt
---

# IAMStreamControl::StopAt


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>StopAt</code> method informs the pin when to stop delivering data.

## -parameters

### -param ptStop [in]

Pointer to a <a href="/windows/desktop/DirectShow/reference-time">REFERENCE_TIME</a> value that specifies when the pin should stop delivering data. If the value is <b>MAXLONGLONG</b> (0x7FFFFFFFFFFFFFFF), the method cancels any previous stop request. If <i>psStop</i> is <b>NULL</b>, the pin stops immediately.

For preview pins, only the values <b>NULL</b> and <b>MAXLONGLONG</b> are valid, because preview pins do not time stamp the samples they deliver.

### -param bSendExtra [in]

Specifies a Boolean value that indicates whether to send an extra sample after the scheduled stop time. If <b>TRUE</b>, the pin sends one extra sample.

### -param dwCookie [in]

Specifies a value to send along with the start notification. See Remarks.

## -returns

If the method succeeds, the return value is S_OK. Otherwise, returns an <b>HRESULT</b> value indicating the cause of the failure.

## -remarks

If the <i>dwCookie</i> parameter is non-zero, the pin will send an <a href="/windows/desktop/DirectShow/ec-stream-control-stopped">EC_STREAM_CONTROL_STOPPED</a> event when it stops delivering data. The first event parameter is a pointer to the pin's <a href="/windows/desktop/api/strmif/nn-strmif-ipin">IPin</a> interface, and the second is the value of <i>dwCookie</i>. If <i>ptStop</i> is <b>NULL</b> or <b>MAXLONGLONG</b>, no event is sent, and the value of <i>dwCookie</i> is ignored.

In video capture, you would typically call this method on the capture filter's output pin and the multiplexer's input pin. The application should wait for the stop event from the multiplexer. This ensures that the capture filter sends the right number of frames, while guaranteeing that all frames reach the multiplexer. Also, set the <i>bSendExtra</i> parameter to <b>TRUE</b> for the capture pin, but <b>FALSE</b> for the multiplexer pin. This causes the capture filter to send one additional frame. The multiplexer relies on the time stamps from the capture pin, so if the extra frame is not sent, the multiplexer will wait indefinitely for the stop time. When the multiplexer receives the extra frame, it will discard it.

This method handles the following boundary conditions:

<ul>
<li>If the stop time falls between the start and stop times of a sample, the pin delivers that sample.</li>
<li>If the start time equals the stop time, the pin delivers one sample.</li>
</ul>
<b>MAXLONGLONG</b> is the largest possible <a href="/windows/desktop/DirectShow/reference-time">REFERENCE_TIME</a> value. In the base class library, it is also defined as the constant <b>MAX_TIME</b>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamstreamcontrol">IAMStreamControl Interface</a>