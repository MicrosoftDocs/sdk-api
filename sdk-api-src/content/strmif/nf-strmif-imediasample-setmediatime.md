---
UID: NF:strmif.IMediaSample.SetMediaTime
title: IMediaSample::SetMediaTime (strmif.h)
description: The SetMediaTime method sets the media times for this sample.
helpviewer_keywords: ["IMediaSample interface [DirectShow]","SetMediaTime method","IMediaSample.SetMediaTime","IMediaSample::SetMediaTime","IMediaSampleSetMediaTime","SetMediaTime","SetMediaTime method [DirectShow]","SetMediaTime method [DirectShow]","IMediaSample interface","dshow.imediasample_setmediatime","strmif/IMediaSample::SetMediaTime"]
old-location: dshow\imediasample_setmediatime.htm
tech.root: dshow
ms.assetid: 8ae9db99-828d-4ac9-aa51-668b84d4dfab
ms.date: 4/26/2023
ms.keywords: IMediaSample interface [DirectShow],SetMediaTime method, IMediaSample.SetMediaTime, IMediaSample::SetMediaTime, IMediaSampleSetMediaTime, SetMediaTime, SetMediaTime method [DirectShow], SetMediaTime method [DirectShow],IMediaSample interface, dshow.imediasample_setmediatime, strmif/IMediaSample::SetMediaTime
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
 - IMediaSample::SetMediaTime
 - strmif/IMediaSample::SetMediaTime
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
 - IMediaSample.SetMediaTime
---

# IMediaSample::SetMediaTime


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetMediaTime</code> method sets the media times for this sample.

## -parameters

### -param pTimeStart [in]

Pointer to the beginning media time.

### -param pTimeEnd [in]

Pointer to the ending media time.

## -returns

Returns S_OK, or an <b>HRESULT</b> value indicating the cause of the error.

## -remarks

To invalidate the media time, set <i>pTimeStart</i> and <i>pTimeEnd</i> to <b>NULL</b>. This will cause the <a href="/windows/desktop/api/strmif/nf-strmif-imediasample-getmediatime">IMediaSample::GetMediaTime</a> method to return VFW_E_MEDIA_TIME_NOT_SET.

For more information about media times, see <a href="/windows/desktop/DirectShow/time-stamps">Time Stamps</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imediasample">IMediaSample Interface</a>