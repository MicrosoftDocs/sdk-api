---
UID: NF:strmif.IAMDevMemoryAllocator.CheckMemory
title: IAMDevMemoryAllocator::CheckMemory (strmif.h)
description: Note  The IAMDevMemoryAllocator interface is deprecated. Tests whether the specific instance (device) of the allocator allocated a memory pointer.
helpviewer_keywords: ["CheckMemory","CheckMemory method [DirectShow]","CheckMemory method [DirectShow]","IAMDevMemoryAllocator interface","IAMDevMemoryAllocator interface [DirectShow]","CheckMemory method","IAMDevMemoryAllocator.CheckMemory","IAMDevMemoryAllocator::CheckMemory","IAMDevMemoryAllocatorCheckMemory","dshow.iamdevmemoryallocator_checkmemory","strmif/IAMDevMemoryAllocator::CheckMemory"]
old-location: dshow\iamdevmemoryallocator_checkmemory.htm
tech.root: dshow
ms.assetid: d51be809-4a97-4098-9ef3-8ed6603f26c0
ms.date: 12/05/2018
ms.keywords: CheckMemory, CheckMemory method [DirectShow], CheckMemory method [DirectShow],IAMDevMemoryAllocator interface, IAMDevMemoryAllocator interface [DirectShow],CheckMemory method, IAMDevMemoryAllocator.CheckMemory, IAMDevMemoryAllocator::CheckMemory, IAMDevMemoryAllocatorCheckMemory, dshow.iamdevmemoryallocator_checkmemory, strmif/IAMDevMemoryAllocator::CheckMemory
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
 - IAMDevMemoryAllocator::CheckMemory
 - strmif/IAMDevMemoryAllocator::CheckMemory
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
 - IAMDevMemoryAllocator.CheckMemory
---

# IAMDevMemoryAllocator::CheckMemory


## -description

<div class="alert"><b>Note</b>  The <b>IAMDevMemoryAllocator</b> interface is deprecated.</div>
<div> </div>
Tests whether the specific instance (device) of the allocator allocated a memory pointer.

## -parameters

### -param pBuffer [in]

Pointer to the allocated memory buffer's address.

## -returns

Returns S_OK if the on-board allocator allocated the memory, or S_FALSE if not. Memory that is on the particular device but not allocated will also return S_FALSE.

## -remarks

The hardware filter typically uses this method to test whether the pointer actually points to on-board memory.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamdevmemoryallocator">IAMDevMemoryAllocator Interface</a>