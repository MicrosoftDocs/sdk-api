---
UID: NN:strmif.IAMDevMemoryAllocator
title: IAMDevMemoryAllocator (strmif.h)
description: Note  This interface is no longer supported by the AVI Splitter. Note  This interface was defined to support older hardware decoders that required AVI files to be read into directly hardware memory.
helpviewer_keywords: ["IAMDevMemoryAllocator","IAMDevMemoryAllocator interface [DirectShow]","IAMDevMemoryAllocator interface [DirectShow]","described","IAMDevMemoryAllocatorInterface","dshow.iamdevmemoryallocator","strmif/IAMDevMemoryAllocator"]
old-location: dshow\iamdevmemoryallocator.htm
tech.root: dshow
ms.assetid: bab1e582-928a-408b-a9c5-8e9827e9928b
ms.date: 4/26/2023
ms.keywords: IAMDevMemoryAllocator, IAMDevMemoryAllocator interface [DirectShow], IAMDevMemoryAllocator interface [DirectShow],described, IAMDevMemoryAllocatorInterface, dshow.iamdevmemoryallocator, strmif/IAMDevMemoryAllocator
req.header: strmif.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMDevMemoryAllocator
 - strmif/IAMDevMemoryAllocator
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmif.h
api_name:
 - IAMDevMemoryAllocator
---

# IAMDevMemoryAllocator interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is no longer supported by the AVI Splitter.</div>
<div> </div>
<div class="alert"><b>Note</b>  This interface was defined to support older hardware decoders that required AVI files to be read into directly hardware memory. The interface enables the AVI parser to allocate memory from the downstream filter but still provide its own allocator.</div>
<div> </div>
Implement this interface when your pin must support the creation of on-board memory allocators. Source filters that are aware of on-board memory and need to create their own allocators should query for this interface, request an amount of memory and then create an allocator (aggregating the device memory control object). Source filters that don't need to create their own allocator could just use the allocator of the downstream pin (which also aggregates the device memory control object). The hardware-based filter can confirm the usage of its on-board memory by calling methods on the aggregated allocator.

Use this interface when applications need to control the memory of codecs with on-board memory.

## -inheritance

The <b>IAMDevMemoryAllocator</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMDevMemoryAllocator</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/deprecated-interfaces">Deprecated Interfaces</a>
