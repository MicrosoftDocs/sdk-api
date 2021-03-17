---
UID: NF:strmif.IAMDevMemoryAllocator.Alloc
title: IAMDevMemoryAllocator::Alloc (strmif.h)
description: Note  The IAMDevMemoryAllocator interface is deprecated. Allocates a memory buffer.
helpviewer_keywords: ["Alloc","Alloc method [DirectShow]","Alloc method [DirectShow]","IAMDevMemoryAllocator interface","IAMDevMemoryAllocator interface [DirectShow]","Alloc method","IAMDevMemoryAllocator.Alloc","IAMDevMemoryAllocator::Alloc","IAMDevMemoryAllocatorAlloc","dshow.iamdevmemoryallocator_alloc","strmif/IAMDevMemoryAllocator::Alloc"]
old-location: dshow\iamdevmemoryallocator_alloc.htm
tech.root: dshow
ms.assetid: de5f7755-fd96-4016-9cab-b98721080e14
ms.date: 12/05/2018
ms.keywords: Alloc, Alloc method [DirectShow], Alloc method [DirectShow],IAMDevMemoryAllocator interface, IAMDevMemoryAllocator interface [DirectShow],Alloc method, IAMDevMemoryAllocator.Alloc, IAMDevMemoryAllocator::Alloc, IAMDevMemoryAllocatorAlloc, dshow.iamdevmemoryallocator_alloc, strmif/IAMDevMemoryAllocator::Alloc
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
 - IAMDevMemoryAllocator::Alloc
 - strmif/IAMDevMemoryAllocator::Alloc
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
 - IAMDevMemoryAllocator.Alloc
---

# IAMDevMemoryAllocator::Alloc


## -description

<div class="alert"><b>Note</b>  The <b>IAMDevMemoryAllocator</b> interface is deprecated.</div>
<div> </div>
Allocates a memory buffer.

## -parameters

### -param ppBuffer [out]

Pointer that will receive the address of the allocated memory buffer.

### -param pdwcbBuffer [in, out]

Pointer to a <b>DWORD</b> whose input value is the number of bytes to allocate and whose output value is the actual number of bytes allocated.

## -returns

Returns S_OK if the desired quantity of memory was allocated, S_FALSE if memory was unavailable.

## -remarks

Call this method to allocate a block of memory from the available pool.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamdevmemoryallocator">IAMDevMemoryAllocator Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamdevmemoryallocator-free">IAMDevMemoryAllocator::Free</a>