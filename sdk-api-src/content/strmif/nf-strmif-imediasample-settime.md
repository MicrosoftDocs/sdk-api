---
UID: NF:strmif.IMediaSample.SetTime
title: IMediaSample::SetTime (strmif.h)
description: The SetTime method sets the stream times when this sample should begin and finish.
helpviewer_keywords: ["IMediaSample interface [DirectShow]","SetTime method","IMediaSample.SetTime","IMediaSample::SetTime","IMediaSampleSetTime","SetTime","SetTime method [DirectShow]","SetTime method [DirectShow]","IMediaSample interface","dshow.imediasample_settime","strmif/IMediaSample::SetTime"]
old-location: dshow\imediasample_settime.htm
tech.root: dshow
ms.assetid: 531eef13-8b04-48d2-9070-7f6e34cacd9e
ms.date: 4/26/2023
ms.keywords: IMediaSample interface [DirectShow],SetTime method, IMediaSample.SetTime, IMediaSample::SetTime, IMediaSampleSetTime, SetTime, SetTime method [DirectShow], SetTime method [DirectShow],IMediaSample interface, dshow.imediasample_settime, strmif/IMediaSample::SetTime
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
 - IMediaSample::SetTime
 - strmif/IMediaSample::SetTime
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
 - IMediaSample.SetTime
---

# IMediaSample::SetTime


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetTime</code> method sets the stream times when this sample should begin and finish.

## -parameters

### -param pTimeStart [in]

Pointer to a variable that contains the start time of the sample.

### -param pTimeEnd [in]

Pointer to a variable that contains the stop time of the sample.

## -returns

Returns S_OK, or <b>HRESULT</b> value indicating the cause of the error.

## -remarks

Both time values are relative to the stream time. For more information, see <a href="/windows/desktop/DirectShow/time-and-clocks-in-directshow">Time and Clocks in DirectShow</a>.

To invalidate the stream times, set <i>pTimeStart</i> and <i>pTimeEnd</i> to <b>NULL</b>. This will cause the <a href="/windows/desktop/api/strmif/nf-strmif-imediasample-gettime">IMediaSample::GetTime</a> method to return VFW_E_SAMPLE_TIME_NOT_SET.

For more information about stream times, see <a href="/windows/desktop/DirectShow/time-and-clocks-in-directshow">Time and Clocks in DirectShow</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imediasample">IMediaSample Interface</a>