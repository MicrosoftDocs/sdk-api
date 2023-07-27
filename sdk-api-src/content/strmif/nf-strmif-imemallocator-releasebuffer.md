---
UID: NF:strmif.IMemAllocator.ReleaseBuffer
title: IMemAllocator::ReleaseBuffer (strmif.h)
description: The ReleaseBuffer method releases a media sample.
helpviewer_keywords: ["IMemAllocator interface [DirectShow]","ReleaseBuffer method","IMemAllocator.ReleaseBuffer","IMemAllocator::ReleaseBuffer","IMemAllocatorReleaseBuffer","ReleaseBuffer","ReleaseBuffer method [DirectShow]","ReleaseBuffer method [DirectShow]","IMemAllocator interface","dshow.imemallocator_releasebuffer","strmif/IMemAllocator::ReleaseBuffer"]
old-location: dshow\imemallocator_releasebuffer.htm
tech.root: dshow
ms.assetid: 96e02a28-af92-41a7-8251-c4ab15190651
ms.date: 4/26/2023
ms.keywords: IMemAllocator interface [DirectShow],ReleaseBuffer method, IMemAllocator.ReleaseBuffer, IMemAllocator::ReleaseBuffer, IMemAllocatorReleaseBuffer, ReleaseBuffer, ReleaseBuffer method [DirectShow], ReleaseBuffer method [DirectShow],IMemAllocator interface, dshow.imemallocator_releasebuffer, strmif/IMemAllocator::ReleaseBuffer
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
 - IMemAllocator::ReleaseBuffer
 - strmif/IMemAllocator::ReleaseBuffer
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
 - IMemAllocator.ReleaseBuffer
---

# IMemAllocator::ReleaseBuffer


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>ReleaseBuffer</code> method releases a media sample.

## -parameters

### -param pBuffer [in]

Pointer to the media sample's <a href="/windows/desktop/api/strmif/nn-strmif-imediasample">IMediaSample</a> interface.

## -returns

Returns S_OK if successful, or an <b>HRESULT</b> value indicating the cause of the error.

## -remarks

When a media sample's reference count reaches zero, it calls this method with itself as the <i>pBuffer</i> parameter. This method releases the sample back to the allocator's list of available samples.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imemallocator">IMemAllocator Interface</a>