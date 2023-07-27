---
UID: NN:strmif.IMemAllocatorCallbackTemp
title: IMemAllocatorCallbackTemp (strmif.h)
description: The IMemAllocatorCallbackTemp interface enables a filter to receive a callback notification from an allocator whenever a sample is returned to the allocator's free list.The use of this interface is deprecated.
helpviewer_keywords: ["IMemAllocatorCallbackTemp","IMemAllocatorCallbackTemp interface [DirectShow]","IMemAllocatorCallbackTemp interface [DirectShow]","described","IMemAllocatorCallbackTempInterface","dshow.imemallocatorcallbacktemp","strmif/IMemAllocatorCallbackTemp"]
old-location: dshow\imemallocatorcallbacktemp.htm
tech.root: dshow
ms.assetid: 6213faaa-86ff-46e7-80da-a043cae40805
ms.date: 4/26/2023
ms.keywords: IMemAllocatorCallbackTemp, IMemAllocatorCallbackTemp interface [DirectShow], IMemAllocatorCallbackTemp interface [DirectShow],described, IMemAllocatorCallbackTempInterface, dshow.imemallocatorcallbacktemp, strmif/IMemAllocatorCallbackTemp
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
 - IMemAllocatorCallbackTemp
 - strmif/IMemAllocatorCallbackTemp
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
 - IMemAllocatorCallbackTemp
---

# IMemAllocatorCallbackTemp interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IMemAllocatorCallbackTemp</code> interface enables a filter to receive a callback notification from an allocator whenever a sample is returned to the allocator's free list.

The use of this interface is deprecated.

## -inheritance

The <b>IMemAllocatorCallbackTemp</b> interface inherits from <a href="/windows/desktop/api/strmif/nn-strmif-imemallocator">IMemAllocator</a>. <b>IMemAllocatorCallbackTemp</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-imemallocator">IMemAllocator</a>
