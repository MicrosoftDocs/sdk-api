---
UID: NF:amstream.IDirectDrawMediaSampleAllocator.GetDirectDraw
title: IDirectDrawMediaSampleAllocator::GetDirectDraw (amstream.h)
description: The GetDirectDraw method retrieves a pointer to the DirectDraw instance used to allocate surfaces.
helpviewer_keywords: ["GetDirectDraw","GetDirectDraw method [DirectShow]","GetDirectDraw method [DirectShow]","IDirectDrawMediaSampleAllocator interface","IDirectDrawMediaSampleAllocator interface [DirectShow]","GetDirectDraw method","IDirectDrawMediaSampleAllocator.GetDirectDraw","IDirectDrawMediaSampleAllocator::GetDirectDraw","IDirectDrawMediaSampleAllocatorGetDirectDraw","amstream/IDirectDrawMediaSampleAllocator::GetDirectDraw","dshow.idirectdrawmediasampleallocator_getdirectdraw"]
old-location: dshow\idirectdrawmediasampleallocator_getdirectdraw.htm
tech.root: dshow
ms.assetid: 6d6eed9d-635d-424b-ba14-213bbe56f66c
ms.date: 4/26/2023
ms.keywords: GetDirectDraw, GetDirectDraw method [DirectShow], GetDirectDraw method [DirectShow],IDirectDrawMediaSampleAllocator interface, IDirectDrawMediaSampleAllocator interface [DirectShow],GetDirectDraw method, IDirectDrawMediaSampleAllocator.GetDirectDraw, IDirectDrawMediaSampleAllocator::GetDirectDraw, IDirectDrawMediaSampleAllocatorGetDirectDraw, amstream/IDirectDrawMediaSampleAllocator::GetDirectDraw, dshow.idirectdrawmediasampleallocator_getdirectdraw
req.header: amstream.h
req.include-header: 
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
 - IDirectDrawMediaSampleAllocator::GetDirectDraw
 - amstream/IDirectDrawMediaSampleAllocator::GetDirectDraw
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
 - IDirectDrawMediaSampleAllocator.GetDirectDraw
---

# IDirectDrawMediaSampleAllocator::GetDirectDraw


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetDirectDraw</code> method retrieves a pointer to the DirectDraw instance used to allocate surfaces.

## -parameters

### -param ppDirectDraw [out]

Address of a pointer that receives the DirectDraw object's <b>IDirectDraw</b> interface.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

The caller should release the returned <b>IDirectDraw</b> pointer, except when calling the <a href="/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a> filter's implementation of this interface.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amstream/nn-amstream-idirectdrawmediasampleallocator">IDirectDrawMediaSampleAllocator Interface</a>