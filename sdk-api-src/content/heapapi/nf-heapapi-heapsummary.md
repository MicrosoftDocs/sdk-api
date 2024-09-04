---
UID: NF:heapapi.HeapSummary
title: HeapSummary
description: The HeapSummary function (heapapi.h) summarizes the specified heap.
ms.date: 08/04/2022
ms.keywords: HeapSummary
targetos: Windows
tech.root: base
req.assembly: 
req.construct-type: function
req.ddi-compliance:
req.dll: kernel32.dll
req.header: heapapi.h
req.idl:
req.include-header:
req.irql:
req.kmdf-ver:
req.lib: kernel32.lib
req.max-support:
req.namespace:
req.redist:
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type:
req.type-library:
req.umdf-ver:
req.unicode-ansi:
f1_keywords:
 - HeapSummary
 - heapapi/HeapSummary
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - kernel32.dll
 - api-ms-win-core-heap-l1-1-0.dll
 - kernelbase.dll
api_name:
 - HeapSummary
---

## -description

Summarizes the specified heap.

## -parameters

### -param hHeap [in]

A handle to the heap to be summarized. This handle is returned by either the
      <a href="/windows/desktop/api/heapapi/nf-heapapi-heapcreate">HeapCreate</a> or
      <a href="/windows/desktop/api/heapapi/nf-heapapi-getprocessheap">GetProcessHeap</a> function.

### -param dwFlags [in]

The heap summary options.  No options are currently defined, pass zero for this parameter.

### -param lpSummary [in, out]

A pointer to a [HEAP_SUMMARY](ns-heapapi-heap_summary.md) structure that receives the information.  Note that you must set the <b>cbSize</b> member to <code>sizeof(HEAP_SUMMARY)</code> before calling this function.

## -returns

Returns TRUE on success, FALSE on failure.

## -remarks

## -see-also
