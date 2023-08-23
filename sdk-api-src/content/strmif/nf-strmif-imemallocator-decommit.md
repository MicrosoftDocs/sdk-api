---
UID: NF:strmif.IMemAllocator.Decommit
title: IMemAllocator::Decommit (strmif.h)
description: The Decommit method releases the buffer memory.
helpviewer_keywords: ["Decommit","Decommit method [DirectShow]","Decommit method [DirectShow]","IMemAllocator interface","IMemAllocator interface [DirectShow]","Decommit method","IMemAllocator.Decommit","IMemAllocator::Decommit","IMemAllocatorDecommit","dshow.imemallocator_decommit","strmif/IMemAllocator::Decommit"]
old-location: dshow\imemallocator_decommit.htm
tech.root: dshow
ms.assetid: 2c1211c1-e047-4240-b85a-9be0a9290d31
ms.date: 4/26/2023
ms.keywords: Decommit, Decommit method [DirectShow], Decommit method [DirectShow],IMemAllocator interface, IMemAllocator interface [DirectShow],Decommit method, IMemAllocator.Decommit, IMemAllocator::Decommit, IMemAllocatorDecommit, dshow.imemallocator_decommit, strmif/IMemAllocator::Decommit
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
 - IMemAllocator::Decommit
 - strmif/IMemAllocator::Decommit
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
 - IMemAllocator.Decommit
---

# IMemAllocator::Decommit


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Decommit</code> method releases the buffer memory.



## -returns

Returns S_OK if successful, or an <b>HRESULT</b> value indicating the cause of the error.

## -remarks

Any threads waiting in the <a href="/windows/desktop/api/strmif/nf-strmif-imemallocator-getbuffer">IMemAllocator::GetBuffer</a> method return with an error. Further calls to <b>GetBuffer</b> fail, until the <a href="/windows/desktop/api/strmif/nf-strmif-imemallocator-commit">IMemAllocator::Commit</a> method is called.

The purpose of the <code>Decommit</code> method is to prevent filters from getting any more samples from the allocator. Filters that already hold a reference count on a sample are not affected. After a filter releases a sample and the reference count goes to zero, however, the sample is no longer available.

The allocator may free the memory belonging to any sample with a reference count of zero. Thus, the <code>Decommit</code> method "releases" the memory in the sense that filters stop having access to it. Whether the memory actually returns to the heap depends on the implementation of the allocator. Some allocators wait until their own destructor method. However, an allocator must not leave any allocated memory behind when it deletes itself. Therefore, an allocator's destructor must wait until all of its samples are released.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imemallocator">IMemAllocator Interface</a>
