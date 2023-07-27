---
UID: NF:strmif.IPin.NewSegment
title: IPin::NewSegment (strmif.h)
description: The NewSegment method notifies the pin that media samples received after this call are grouped as a segment, with a common start time, stop time, and rate.
helpviewer_keywords: ["IPin interface [DirectShow]","NewSegment method","IPin.NewSegment","IPin::NewSegment","IPinNewSegment","NewSegment","NewSegment method [DirectShow]","NewSegment method [DirectShow]","IPin interface","dshow.ipin_newsegment","strmif/IPin::NewSegment"]
old-location: dshow\ipin_newsegment.htm
tech.root: dshow
ms.assetid: 70c4bda0-3efa-4f85-b71e-174c4c80830c
ms.date: 4/26/2023
ms.keywords: IPin interface [DirectShow],NewSegment method, IPin.NewSegment, IPin::NewSegment, IPinNewSegment, NewSegment, NewSegment method [DirectShow], NewSegment method [DirectShow],IPin interface, dshow.ipin_newsegment, strmif/IPin::NewSegment
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
 - IPin::NewSegment
 - strmif/IPin::NewSegment
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
 - IPin.NewSegment
---

# IPin::NewSegment


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>NewSegment</code> method notifies the pin that media samples received after this call are grouped as a segment, with a common start time, stop time, and rate.



Applications should not call this method. This method is called by other filters.

## -parameters

### -param tStart

Start time of the segment, relative to the original source, in 100-nanosecond units.

### -param tStop

End time of the segment, relative to the original source, in 100-nanosecond units.

### -param dRate

Rate at which this segment should be processed, as a percentage of the original rate.

## -returns

Returns S_OK if successful, or an <b>HRESULT</b> value indicating the cause of the error.

## -remarks

A source filter (or parser filter) calls this method at the start of each new stream and after each seek operation. It calls the method on the input pin of the downstream filter, after delivering the previous batch of data and before calling <a href="/windows/desktop/api/strmif/nf-strmif-imeminputpin-receive">IMemInputPin::Receive</a> with any new data. The downstream filter propagates the <code>NewSegment</code> call downstream.

Filters can use segment information to process samples. For example, with some formats it is impossible to reconstruct a delta frame without the next key frame. Therefore, if the stop time occurs on a delta frame, the source filter must send some additional frames. The decoder filter determines the final frame based on the segment information. The segment rate is used to render continuous data sources, such as audio data. For example, the audio renderer uses the sampling rate and the segment rate to render the audio data correctly.

## -see-also

<a href="/windows/desktop/DirectShow/data-flow-in-the-filter-graph">Data Flow in the Filter Graph</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ipin">IPin Interface</a>