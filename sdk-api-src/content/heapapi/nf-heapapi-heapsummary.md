---
UID: NF:heapapi.HeapSummary
title: HeapSummary
ms.date: 4/26/2019
ms.keywords: HeapSummary
ms.topic: language-reference
targetos: Windows
product: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: heapapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - api-ms-win-core-heap-l1-1-0.dll
api_name:
 - HeapSummary
---

## -description

Summarizes the specified heap.


## -parameters

### -param hHeap

A handle to the heap to be summarized. This handle is returned by either the 
      <a href="https://docs.microsoft.com/windows/desktop/api/heapapi/nf-heapapi-heapcreate">HeapCreate</a> or 
      <a href="https://docs.microsoft.com/windows/desktop/api/heapapi/nf-heapapi-getprocessheap">GetProcessHeap</a> function.

### -param dwFlags

The heap summary options.

### -param lpSummary

Receives a pointer to a [Heap_Summary](ns-heapapi-heap_summary) structure representing the heap summary.

## -returns

Returns S_OK on success.

## -remarks

## -see-also

