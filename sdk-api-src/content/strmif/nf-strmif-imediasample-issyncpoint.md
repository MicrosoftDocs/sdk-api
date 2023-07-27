---
UID: NF:strmif.IMediaSample.IsSyncPoint
title: IMediaSample::IsSyncPoint (strmif.h)
description: The IsSyncPoint method determines if the beginning of this sample is a synchronization point.
helpviewer_keywords: ["IMediaSample interface [DirectShow]","IsSyncPoint method","IMediaSample.IsSyncPoint","IMediaSample::IsSyncPoint","IMediaSampleIsSyncPoint","IsSyncPoint","IsSyncPoint method [DirectShow]","IsSyncPoint method [DirectShow]","IMediaSample interface","dshow.imediasample_issyncpoint","strmif/IMediaSample::IsSyncPoint"]
old-location: dshow\imediasample_issyncpoint.htm
tech.root: dshow
ms.assetid: eed64bd9-1300-4db3-a3ed-c7e8ff9c7c8f
ms.date: 4/26/2023
ms.keywords: IMediaSample interface [DirectShow],IsSyncPoint method, IMediaSample.IsSyncPoint, IMediaSample::IsSyncPoint, IMediaSampleIsSyncPoint, IsSyncPoint, IsSyncPoint method [DirectShow], IsSyncPoint method [DirectShow],IMediaSample interface, dshow.imediasample_issyncpoint, strmif/IMediaSample::IsSyncPoint
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
 - IMediaSample::IsSyncPoint
 - strmif/IMediaSample::IsSyncPoint
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
 - IMediaSample.IsSyncPoint
---

# IMediaSample::IsSyncPoint


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IsSyncPoint</code> method determines if the beginning of this sample is a synchronization point.



## -returns

Returns S_OK if the sample is a synchronization point. Otherwise, returns S_FALSE.

## -remarks

A filter can begin a stream at any synchronization point. With some compression types, streaming can begin only at certain points in the stream; for example, on key frames. If the <b>bTemporalCompression</b> member of the <a href="/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a> structure is <b>FALSE</b>, all samples are synchronization points.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imediasample">IMediaSample Interface</a>
