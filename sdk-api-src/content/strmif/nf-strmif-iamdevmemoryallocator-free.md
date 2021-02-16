---
UID: NF:strmif.IAMDevMemoryAllocator.Free
title: IAMDevMemoryAllocator::Free (strmif.h)
description: Note  The IAMDevMemoryAllocator interface is deprecated. Frees the previously allocated memory.
helpviewer_keywords: ["Free","Free method [DirectShow]","Free method [DirectShow]","IAMDevMemoryAllocator interface","IAMDevMemoryAllocator interface [DirectShow]","Free method","IAMDevMemoryAllocator.Free","IAMDevMemoryAllocator::Free","IAMDevMemoryAllocatorFree","dshow.iamdevmemoryallocator_free","strmif/IAMDevMemoryAllocator::Free"]
old-location: dshow\iamdevmemoryallocator_free.htm
tech.root: dshow
ms.assetid: d86d3016-bca0-4a0b-946b-f50c49266c67
ms.date: 12/05/2018
ms.keywords: Free, Free method [DirectShow], Free method [DirectShow],IAMDevMemoryAllocator interface, IAMDevMemoryAllocator interface [DirectShow],Free method, IAMDevMemoryAllocator.Free, IAMDevMemoryAllocator::Free, IAMDevMemoryAllocatorFree, dshow.iamdevmemoryallocator_free, strmif/IAMDevMemoryAllocator::Free
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
 - IAMDevMemoryAllocator::Free
 - strmif/IAMDevMemoryAllocator::Free
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
 - IAMDevMemoryAllocator.Free
---

# IAMDevMemoryAllocator::Free


## -description

<div class="alert"><b>Note</b>  The <b>IAMDevMemoryAllocator</b> interface is deprecated.</div>
<div> </div>
Frees the previously allocated memory.

## -parameters

### -param pBuffer [in]

Pointer to the allocated memory.

## -returns

Returns E_INVALIDARG if the specified allocator didn't allocate the memory (that is, <a href="/windows/desktop/api/strmif/nf-strmif-iamdevmemoryallocator-checkmemory">CheckMemory</a> fails).

## -remarks

This method frees a block of memory from the pool.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamdevmemoryallocator">IAMDevMemoryAllocator Interface</a>