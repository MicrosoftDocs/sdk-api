---
UID: NF:strmif.IMediaSeeking.SetRate
title: IMediaSeeking::SetRate (strmif.h)
description: The SetRate method sets the playback rate.
helpviewer_keywords: ["IMediaSeeking interface [DirectShow]","SetRate method","IMediaSeeking.SetRate","IMediaSeeking::SetRate","IMediaSeekingSetRate","SetRate","SetRate method [DirectShow]","SetRate method [DirectShow]","IMediaSeeking interface","dshow.imediaseeking_setrate","strmif/IMediaSeeking::SetRate"]
old-location: dshow\imediaseeking_setrate.htm
tech.root: dshow
ms.assetid: 8cd44480-cadb-4b59-9fe7-4a82b3aed15b
ms.date: 4/26/2023
ms.keywords: IMediaSeeking interface [DirectShow],SetRate method, IMediaSeeking.SetRate, IMediaSeeking::SetRate, IMediaSeekingSetRate, SetRate, SetRate method [DirectShow], SetRate method [DirectShow],IMediaSeeking interface, dshow.imediaseeking_setrate, strmif/IMediaSeeking::SetRate
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
 - IMediaSeeking::SetRate
 - strmif/IMediaSeeking::SetRate
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
 - IMediaSeeking.SetRate
---

# IMediaSeeking::SetRate


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetRate</code> method sets the playback rate.

## -parameters

### -param dRate [in]

Playback rate. Must not be zero.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The specified rate was zero or a negative value. (See Remarks.)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_UNSUPPORTED_AUDIO</b></dt>
</dl>
</td>
<td width="60%">
Audio device or filter does not support this rate.

</td>
</tr>
</table>

## -remarks

The playback rate is expressed as a ratio of the normal speed. Thus, 1.0 is normal playback speed, 0.5 is half speed, and 2.0 is twice speed. For audio streams, changing the rate also changes the pitch.

Negative values indicate reverse playback. Most filters do not support negative playback, but instead return an error code if the <i>dRate</i> parameter is negative.

When an application calls this method on the Filter Graph Manager, the Filter Graph Manager does the following:

<ol>
<li>Calls the <a href="/windows/desktop/api/strmif/nf-strmif-imediaseeking-getcurrentposition">IMediaSeeking::GetCurrentPosition</a> method. This call returns the current position as calculated by the Filter Graph Manager.</li>
<li>Stops the filter graph (if the graph is paused or running).</li>
<li>Calls the <a href="/windows/desktop/api/strmif/nf-strmif-imediaseeking-setpositions">IMediaSeeking::SetPositions</a> method on the filters, with the current position as the start time. This has the effect of resetting the stream time to zero.</li>
<li>Calls the <code>SetRate</code> method on the filters, with the new rate.</li>
<li>Resumes the filter graph, if it was paused or running.</li>
</ol>
If an error occurs in step 4, the Filter Graph Manager tries to restore the previous rate.

Filters should respond to rate changes as follows:

<b>Parser and source filters: </b>The filter that originates the timestamps responds to the <code>SetRate</code> call. This is usually a parser filter, such as the <a href="/windows/desktop/DirectShow/avi-splitter-filter">AVI Splitter Filter</a>, but it might be a source filter. After any seek or rate change, the filter should call the <a href="/windows/desktop/api/strmif/nf-strmif-ipin-newsegment">IPin::NewSegment</a> method with the new settings. After a rate change, it should adjust its timestamps accordingly. Because a rate change is preceded by a seek, timestamps restart from zero, so the filter can simply divide by the rate to calculate the new timestamps.

<b>Decoder filters: </b>Decoders should not act on <code>SetRate</code> calls other than to pass them upstream. Instead, they should respond to the <b>NewSegment</b> call that the upstream parser issues. When a decoder filter receives new segment information, it should store the values and pass the <b>NewSegment</b> call downstream. Some decoders need to generate extra timestamps by interpolating their input; they should take rate changes into account when doing so.

<b>Renderers: </b>Video renderers can typically ignore rate changes, because the incoming frames already have the correct time stamp. Audio renderers must modify their playback rate, because audio decoders typically do not make rate-change conversions.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imediaseeking">IMediaSeeking Interface</a>