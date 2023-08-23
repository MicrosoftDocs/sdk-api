---
UID: NF:strmif.IMediaSample.SetSyncPoint
title: IMediaSample::SetSyncPoint (strmif.h)
description: The SetSyncPoint method specifies whether the beginning of this sample is a synchronization point.
helpviewer_keywords: ["IMediaSample interface [DirectShow]","SetSyncPoint method","IMediaSample.SetSyncPoint","IMediaSample::SetSyncPoint","IMediaSampleSetSyncPoint","SetSyncPoint","SetSyncPoint method [DirectShow]","SetSyncPoint method [DirectShow]","IMediaSample interface","dshow.imediasample_setsyncpoint","strmif/IMediaSample::SetSyncPoint"]
old-location: dshow\imediasample_setsyncpoint.htm
tech.root: dshow
ms.assetid: b2770045-c18b-4dbc-b104-873e07c0b5aa
ms.date: 4/26/2023
ms.keywords: IMediaSample interface [DirectShow],SetSyncPoint method, IMediaSample.SetSyncPoint, IMediaSample::SetSyncPoint, IMediaSampleSetSyncPoint, SetSyncPoint, SetSyncPoint method [DirectShow], SetSyncPoint method [DirectShow],IMediaSample interface, dshow.imediasample_setsyncpoint, strmif/IMediaSample::SetSyncPoint
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
 - IMediaSample::SetSyncPoint
 - strmif/IMediaSample::SetSyncPoint
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
 - IMediaSample.SetSyncPoint
---

# IMediaSample::SetSyncPoint


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetSyncPoint</code> method specifies whether the beginning of this sample is a synchronization point.

## -parameters

### -param bIsSyncPoint [in]

Boolean value that specifies whether this is a synchronization point. If <b>TRUE</b>, this is a synchronization point.

## -returns

Returns S_OK or an <b>HRESULT</b> value indicating the cause of the error.

## -remarks

The filter that first generates the data in the sample should set this flag to <b>TRUE</b> or <b>FALSE</b>, as appropriate. For uncompressed video and PCM audio, set every sample to <b>TRUE</b>. For compressed video, set key frames to <b>TRUE</b> and delta frames to <b>FALSE</b>.

This flag is purely informational. Other filters downstream might check this flag; for example, a filter might need to skip to the next key frame.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imediasample">IMediaSample Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-imediasample-issyncpoint">IMediaSample::IsSyncPoint</a>