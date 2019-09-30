---
UID: NS:heapapi._HEAP_SUMMARY
title: HEAP_SUMMARY
ms.date: 4/26/2019
ms.keywords: _HEAP_SUMMARY, HEAP_SUMMARY
ms.topic: language-reference
targetos: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: heapapi.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: HEAP_SUMMARY, *PHEAP_SUMMARY
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - heapapi.h
api_name:
 - _HEAP_SUMMARY
 - HEAP_SUMMARY
---

## -description

Represents a heap summary retrieved with a call to [HeapSummary](nf-heapapi-heapsummary)

## -struct-fields

### -field cb

Address of a continuous block of memory.

### -field cbAllocated

The size of the allocated memory.

### -field cbCommitted

The size of the committed memory.


### -field cbReserved

The size of the reserved memory.

### -field cbMaxReserve

The size of the maximum reserved memory.

## -remarks

## -see-also

