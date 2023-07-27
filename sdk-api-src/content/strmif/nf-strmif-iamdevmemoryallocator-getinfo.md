---
UID: NF:strmif.IAMDevMemoryAllocator.GetInfo
title: IAMDevMemoryAllocator::GetInfo (strmif.h)
description: Note  The IAMDevMemoryAllocator interface is deprecated. Retrieves information about the memory capabilities.
helpviewer_keywords: ["GetInfo","GetInfo method [DirectShow]","GetInfo method [DirectShow]","IAMDevMemoryAllocator interface","IAMDevMemoryAllocator interface [DirectShow]","GetInfo method","IAMDevMemoryAllocator.GetInfo","IAMDevMemoryAllocator::GetInfo","IAMDevMemoryAllocatorGetInfo","dshow.iamdevmemoryallocator_getinfo","strmif/IAMDevMemoryAllocator::GetInfo"]
old-location: dshow\iamdevmemoryallocator_getinfo.htm
tech.root: dshow
ms.assetid: ee3070ed-98df-4f20-a91f-bb3c3492f3d8
ms.date: 4/26/2023
ms.keywords: GetInfo, GetInfo method [DirectShow], GetInfo method [DirectShow],IAMDevMemoryAllocator interface, IAMDevMemoryAllocator interface [DirectShow],GetInfo method, IAMDevMemoryAllocator.GetInfo, IAMDevMemoryAllocator::GetInfo, IAMDevMemoryAllocatorGetInfo, dshow.iamdevmemoryallocator_getinfo, strmif/IAMDevMemoryAllocator::GetInfo
req.header: strmif.h
req.include-header: Dshow.h
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
 - IAMDevMemoryAllocator::GetInfo
 - strmif/IAMDevMemoryAllocator::GetInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IAMDevMemoryAllocator.GetInfo
---

# IAMDevMemoryAllocator::GetInfo


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  The <b>IAMDevMemoryAllocator</b> interface is deprecated.</div>
<div> </div>
Retrieves information about the memory capabilities.

## -parameters

### -param pdwcbTotalFree [out]

Pointer to the total free memory size.

### -param pdwcbLargestFree [out]

Pointer to the returned largest free memory size.

### -param pdwcbTotalMemory [out]

Pointer to the returned total memory size.

### -param pdwcbMinimumChunk [out]

Pointer to the returned minimum chunk size, giving granularity and alignment rules.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

Use this method to find out the total amount of memory available. This method returns values for the entire on-board memory that is available on that device. If multiple filters (devices) share the memory, it will return the amount available to that specific device, which might be a portion of the total amount of on-board memory. This amount will be implementation-specific. For example, the on-board memory manager on the codec might be able to access all 32 megabytes (MB) of memory on the card. However, individual pin implementations of <a href="/windows/desktop/api/strmif/nn-strmif-iamdevmemoryallocator">IAMDevMemoryAllocator</a> only report a portion of this memory.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamdevmemoryallocator">IAMDevMemoryAllocator Interface</a>