---
UID: NS:heapapi._HEAP_SUMMARY
title: HEAP_SUMMARY
description: The HEAP_SUMMARY structure (heapapi.h) represents a heap summary retrieved with a call to the HeapSummary function.
ms.date: 08/04/2022
ms.keywords: _HEAP_SUMMARY, HEAP_SUMMARY
tech.root: base
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
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.typenames: HEAP_SUMMARY, *PHEAP_SUMMARY
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - _HEAP_SUMMARY
 - heapapi/_HEAP_SUMMARY
 - PHEAP_SUMMARY
 - heapapi/PHEAP_SUMMARY
 - HEAP_SUMMARY
 - heapapi/HEAP_SUMMARY
dev_langs:
 - c++
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

Represents a heap summary retrieved with a call to [HeapSummary](nf-heapapi-heapsummary.md)

## -struct-fields

### -field cb

The size of this data structure, in bytes. Set this member to sizeof(HEAP_SUMMARY).

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

