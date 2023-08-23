---
UID: NF:strmif.IMediaSample.GetPointer
title: IMediaSample::GetPointer (strmif.h)
description: The GetPointer method retrieves a read/write pointer to the media sample's buffer.
helpviewer_keywords: ["GetPointer","GetPointer method [DirectShow]","GetPointer method [DirectShow]","IMediaSample interface","IMediaSample interface [DirectShow]","GetPointer method","IMediaSample.GetPointer","IMediaSample::GetPointer","IMediaSampleGetPointer","dshow.imediasample_getpointer","strmif/IMediaSample::GetPointer"]
old-location: dshow\imediasample_getpointer.htm
tech.root: dshow
ms.assetid: a3c69dfb-6ee4-401b-8dcb-4e42a8cd8156
ms.date: 4/26/2023
ms.keywords: GetPointer, GetPointer method [DirectShow], GetPointer method [DirectShow],IMediaSample interface, IMediaSample interface [DirectShow],GetPointer method, IMediaSample.GetPointer, IMediaSample::GetPointer, IMediaSampleGetPointer, dshow.imediasample_getpointer, strmif/IMediaSample::GetPointer
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
 - IMediaSample::GetPointer
 - strmif/IMediaSample::GetPointer
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
 - IMediaSample.GetPointer
---

# IMediaSample::GetPointer


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetPointer</code> method retrieves a read/write pointer to the media sample's buffer.

## -parameters

### -param ppBuffer [out]

Receives a pointer to the buffer.

## -returns

Returns S_OK if successful, or an <b>HRESULT</b> value indicating the cause of the error.

## -remarks

The buffer memory is owned by the media sample object, and is automatically released when the media sample is destroyed. The caller should not free or reallocate the buffer.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imediasample">IMediaSample Interface</a>