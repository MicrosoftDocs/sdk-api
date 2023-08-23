---
UID: NF:strmif.IMediaSample.IsDiscontinuity
title: IMediaSample::IsDiscontinuity (strmif.h)
description: The IsDiscontinuity method determines if this sample represents a break in the data stream.
helpviewer_keywords: ["IMediaSample interface [DirectShow]","IsDiscontinuity method","IMediaSample.IsDiscontinuity","IMediaSample::IsDiscontinuity","IMediaSampleIsDiscontinuity","IsDiscontinuity","IsDiscontinuity method [DirectShow]","IsDiscontinuity method [DirectShow]","IMediaSample interface","dshow.imediasample_isdiscontinuity","strmif/IMediaSample::IsDiscontinuity"]
old-location: dshow\imediasample_isdiscontinuity.htm
tech.root: dshow
ms.assetid: 0bab511e-a744-4b6e-afe3-0ceb473dfcae
ms.date: 4/26/2023
ms.keywords: IMediaSample interface [DirectShow],IsDiscontinuity method, IMediaSample.IsDiscontinuity, IMediaSample::IsDiscontinuity, IMediaSampleIsDiscontinuity, IsDiscontinuity, IsDiscontinuity method [DirectShow], IsDiscontinuity method [DirectShow],IMediaSample interface, dshow.imediasample_isdiscontinuity, strmif/IMediaSample::IsDiscontinuity
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
 - IMediaSample::IsDiscontinuity
 - strmif/IMediaSample::IsDiscontinuity
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
 - IMediaSample.IsDiscontinuity
---

# IMediaSample::IsDiscontinuity


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IsDiscontinuity</code> method determines if this sample represents a break in the data stream.



## -returns

Returns S_OK if the sample is a break in the data stream. Otherwise, returns S_FALSE.

## -remarks

A discontinuity occurs when a filter seeks to a different place in the stream, or when a filter drops samples for quality control.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imediasample">IMediaSample Interface</a>
