---
UID: NF:strmif.IMediaSample.SetDiscontinuity
title: IMediaSample::SetDiscontinuity (strmif.h)
description: The SetDiscontinuity method specifies whether this sample represents a break in the data stream.
helpviewer_keywords: ["IMediaSample interface [DirectShow]","SetDiscontinuity method","IMediaSample.SetDiscontinuity","IMediaSample::SetDiscontinuity","IMediaSampleSetDiscontinuity","SetDiscontinuity","SetDiscontinuity method [DirectShow]","SetDiscontinuity method [DirectShow]","IMediaSample interface","dshow.imediasample_setdiscontinuity","strmif/IMediaSample::SetDiscontinuity"]
old-location: dshow\imediasample_setdiscontinuity.htm
tech.root: dshow
ms.assetid: 57041c71-4c7e-463a-92f5-c77a76aa545a
ms.date: 4/26/2023
ms.keywords: IMediaSample interface [DirectShow],SetDiscontinuity method, IMediaSample.SetDiscontinuity, IMediaSample::SetDiscontinuity, IMediaSampleSetDiscontinuity, SetDiscontinuity, SetDiscontinuity method [DirectShow], SetDiscontinuity method [DirectShow],IMediaSample interface, dshow.imediasample_setdiscontinuity, strmif/IMediaSample::SetDiscontinuity
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
 - IMediaSample::SetDiscontinuity
 - strmif/IMediaSample::SetDiscontinuity
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
 - IMediaSample.SetDiscontinuity
---

# IMediaSample::SetDiscontinuity


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetDiscontinuity</code> method specifies whether this sample represents a break in the data stream.

## -parameters

### -param bDiscontinuity [in]

Boolean value that specifies whether this sample is a discontinuity. If <b>TRUE</b>, the media sample is discontinuous with the previous sample.

## -returns

Returns S_OK, or an <b>HRESULT</b> value indicating the cause of the error.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imediasample">IMediaSample Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-imediasample-isdiscontinuity">IMediaSample::IsDiscontinuity</a>