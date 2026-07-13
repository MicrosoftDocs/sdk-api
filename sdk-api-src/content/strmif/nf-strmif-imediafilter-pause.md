---
UID: NF:strmif.IMediaFilter.Pause
title: IMediaFilter::Pause (strmif.h)
description: The Pause method pauses the filter.
helpviewer_keywords: ["IBaseFilter interface [DirectShow]","Pause method","IBaseFilter::Pause","IMediaFilter interface [DirectShow]","Pause method","IMediaFilter.Pause","IMediaFilter::Pause","IMediaFilterPause","Pause","Pause method [DirectShow]","Pause method [DirectShow]","IBaseFilter interface","Pause method [DirectShow]","IMediaFilter interface","dshow.imediafilter_pause","strmif/IBaseFilter::Pause","strmif/IMediaFilter::Pause"]
old-location: dshow\imediafilter_pause.htm
tech.root: dshow
ms.assetid: 0dbd79be-8f44-4bac-b117-03e6316693f8
ms.date: 4/26/2023
ms.keywords: IBaseFilter interface [DirectShow],Pause method, IBaseFilter::Pause, IMediaFilter interface [DirectShow],Pause method, IMediaFilter.Pause, IMediaFilter::Pause, IMediaFilterPause, Pause, Pause method [DirectShow], Pause method [DirectShow],IBaseFilter interface, Pause method [DirectShow],IMediaFilter interface, dshow.imediafilter_pause, strmif/IBaseFilter::Pause, strmif/IMediaFilter::Pause
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
 - IMediaFilter::Pause
 - strmif/IMediaFilter::Pause
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
 - IMediaFilter.Pause
 - IBaseFilter.Pause
---

# IMediaFilter::Pause


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>Pause</b> method pauses the filter.



## -returns

Returns an <b>HRESULT</b> value. Possible values include those shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Transition is not complete.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success. Transition is complete.

</td>
</tr>
</table>

## -remarks

When a filter is paused, it can receive, process, and deliver samples. However, a renderer filter will only accept one sample while paused. Therefore, when the filter graph is paused, samples move through the graph until the first sample reaches the renderer. At that point, streaming is paused until the <a href="/windows/desktop/api/strmif/nf-strmif-imediafilter-run">IMediaFilter::Run</a> method is called. Video renderers display the first sample as a still frame.
      

Live capture filters do not deliver any samples while paused, only while running.
      

The state transition might be asynchronous. If the method returns before the transition completes, the return value is <b>S_FALSE</b>. A renderer filter does not complete the transition to paused until either (1) it receives one sample, or (2) it receives an end-of-stream notification. While the state transition is pending, <a href="/windows/desktop/api/strmif/nf-strmif-imediafilter-getstate">IMediaFilter::GetState</a> returns <b>VFW_S_STATE_INTERMEDIATE</b>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imediafilter">IMediaFilter Interface</a>
