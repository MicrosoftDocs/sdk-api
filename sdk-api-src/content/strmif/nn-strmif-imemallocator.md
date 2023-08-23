---
UID: NN:strmif.IMemAllocator
title: IMemAllocator (strmif.h)
description: The IMemAllocator interface allocates media samples, for moving data between pins.This interface is used by pins that share allocators, when the input pin exposes the IMemInputPin interface.
helpviewer_keywords: ["IMemAllocator","IMemAllocator interface [DirectShow]","IMemAllocator interface [DirectShow]","described","IMemAllocatorInterface","dshow.imemallocator","strmif/IMemAllocator"]
old-location: dshow\imemallocator.htm
tech.root: dshow
ms.assetid: 77a161c4-706c-4270-a343-9e16c03cd590
ms.date: 4/26/2023
ms.keywords: IMemAllocator, IMemAllocator interface [DirectShow], IMemAllocator interface [DirectShow],described, IMemAllocatorInterface, dshow.imemallocator, strmif/IMemAllocator
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
 - IMemAllocator
 - strmif/IMemAllocator
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
 - IMemAllocator
---

# IMemAllocator interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IMemAllocator</code> interface allocates media samples, for moving data between pins.

This interface is used by pins that share allocators, when the input pin exposes the <a href="/windows/desktop/api/strmif/nn-strmif-imeminputpin">IMemInputPin</a> interface. The pins negotiate which pin will provide the allocator. The allocator is used to allocate memory buffers, retrieve empty buffers, and release buffers. Not every filter creates its own allocator, so one allocator might be used by several filters. For more information, see <a href="/windows/desktop/DirectShow/how-filters-connect">How Filters Connect</a>.

Applications typically do not use this interface.

To use an allocator, perform the following steps:

<ol>
<li>Call the <a href="/windows/desktop/api/strmif/nf-strmif-imemallocator-setproperties">IMemAllocator::SetProperties</a> method to specify the buffer requirements, including the number of buffers and the size of each buffer.</li>
<li>Call the <a href="/windows/desktop/api/strmif/nf-strmif-imemallocator-commit">IMemAllocator::Commit</a> method to allocate the buffers.</li>
<li>Call the <a href="/windows/desktop/api/strmif/nf-strmif-imemallocator-getbuffer">IMemAllocator::GetBuffer</a> method to retrieve media samples. This method blocks until the next sample becomes available.</li>
<li>When you are done with each sample, call the <b>IUnknown::Release</b> method on the sample. The sample is not deleted when its reference count reaches zero. Instead, the sample returns to the allocator's free list.</li>
<li>When you are done using the allocator, call the <a href="/windows/desktop/api/strmif/nf-strmif-imemallocator-decommit">IMemAllocator::Decommit</a> method to release the memory for the buffers.</li>
</ol>

## -inheritance

The <b>IMemAllocator</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMemAllocator</b> also has these types of members:

