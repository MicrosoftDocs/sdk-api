---
UID: NF:strmif.IMediaSeeking.GetDuration
title: IMediaSeeking::GetDuration (strmif.h)
description: The GetDuration method gets the duration of the stream.
helpviewer_keywords: ["GetDuration","GetDuration method [DirectShow]","GetDuration method [DirectShow]","IMediaSeeking interface","IMediaSeeking interface [DirectShow]","GetDuration method","IMediaSeeking.GetDuration","IMediaSeeking::GetDuration","IMediaSeekingGetDuration","dshow.imediaseeking_getduration","strmif/IMediaSeeking::GetDuration"]
old-location: dshow\imediaseeking_getduration.htm
tech.root: dshow
ms.assetid: 15b98fb0-a0dd-47fc-8046-fa336afa970c
ms.date: 4/26/2023
ms.keywords: GetDuration, GetDuration method [DirectShow], GetDuration method [DirectShow],IMediaSeeking interface, IMediaSeeking interface [DirectShow],GetDuration method, IMediaSeeking.GetDuration, IMediaSeeking::GetDuration, IMediaSeekingGetDuration, dshow.imediaseeking_getduration, strmif/IMediaSeeking::GetDuration
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
 - IMediaSeeking::GetDuration
 - strmif/IMediaSeeking::GetDuration
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
 - IMediaSeeking.GetDuration
---

# IMediaSeeking::GetDuration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetDuration</b> method gets the duration of the stream.

## -parameters

### -param pDuration [out]

Receives the duration, in units of the current time format.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method gets the duration of the stream at normal playback speed. Changing the playback rate does not affect the duration.
      

The duration is expressed in the current time format. The default time format is <a href="/windows/desktop/DirectShow/reference-time">REFERENCE_TIME</a> units (100 nanoseconds). To change time formats, use the <a href="/windows/desktop/api/strmif/nf-strmif-imediaseeking-settimeformat">IMediaSeeking::SetTimeFormat</a> method.
      

Depending on the source format, the duration might not be exact. For example, if the source contains a variable bit-rate (VBR) stream, the method might return an estimated duration.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imediaseeking">IMediaSeeking Interface</a>