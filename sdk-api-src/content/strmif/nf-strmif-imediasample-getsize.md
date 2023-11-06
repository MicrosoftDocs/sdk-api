---
UID: NF:strmif.IMediaSample.GetSize
title: IMediaSample::GetSize (strmif.h)
description: The GetSize method retrieves the size of the buffer.
helpviewer_keywords: ["GetSize","GetSize method [DirectShow]","GetSize method [DirectShow]","IMediaSample interface","IMediaSample interface [DirectShow]","GetSize method","IMediaSample.GetSize","IMediaSample::GetSize","IMediaSampleGetSize","dshow.imediasample_getsize","strmif/IMediaSample::GetSize"]
old-location: dshow\imediasample_getsize.htm
tech.root: dshow
ms.assetid: 6dc50db2-dc75-4c04-ac30-78275ee35ce8
ms.date: 4/26/2023
ms.keywords: GetSize, GetSize method [DirectShow], GetSize method [DirectShow],IMediaSample interface, IMediaSample interface [DirectShow],GetSize method, IMediaSample.GetSize, IMediaSample::GetSize, IMediaSampleGetSize, dshow.imediasample_getsize, strmif/IMediaSample::GetSize
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
 - IMediaSample::GetSize
 - strmif/IMediaSample::GetSize
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
 - IMediaSample.GetSize
---

# IMediaSample::GetSize


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetSize</code> method retrieves the size of the buffer.



## -returns

Returns the size of the buffer, in bytes. The size does not include the prefix bytes, if any.

## -see-also

[ALLOCATOR_PROPERTIES](/windows/desktop/api/strmif/ns-strmif-allocator_properties)



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imediasample">IMediaSample Interface</a>
