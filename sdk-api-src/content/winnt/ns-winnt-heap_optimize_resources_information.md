---
UID: NS:winnt._HEAP_OPTIMIZE_RESOURCES_INFORMATION
title: HEAP_OPTIMIZE_RESOURCES_INFORMATION (winnt.h)
description: Specifies flags for a HeapOptimizeResources operation initiated with HeapSetInformation.
helpviewer_keywords: ["*PHEAP_OPTIMIZE_RESOURCES_INFORMATION","HEAP_OPTIMIZE_RESOURCES_INFORMATION","HEAP_OPTIMIZE_RESOURCES_INFORMATION structure","PHEAP_OPTIMIZE_RESOURCES_INFORMATION","PHEAP_OPTIMIZE_RESOURCES_INFORMATION structure pointer","base.heap_optimize_resources_information","winnt/HEAP_OPTIMIZE_RESOURCES_INFORMATION","winnt/PHEAP_OPTIMIZE_RESOURCES_INFORMATION"]
old-location: base\heap_optimize_resources_information.htm
tech.root: base
ms.assetid: c801a08a-0b1a-4ffe-8ec7-c3ea8d913ec8
ms.date: 12/05/2018
ms.keywords: '*PHEAP_OPTIMIZE_RESOURCES_INFORMATION, HEAP_OPTIMIZE_RESOURCES_INFORMATION, HEAP_OPTIMIZE_RESOURCES_INFORMATION structure, PHEAP_OPTIMIZE_RESOURCES_INFORMATION, PHEAP_OPTIMIZE_RESOURCES_INFORMATION structure pointer, base.heap_optimize_resources_information, winnt/HEAP_OPTIMIZE_RESOURCES_INFORMATION, winnt/PHEAP_OPTIMIZE_RESOURCES_INFORMATION'
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
req.typenames: HEAP_OPTIMIZE_RESOURCES_INFORMATION, *PHEAP_OPTIMIZE_RESOURCES_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HEAP_OPTIMIZE_RESOURCES_INFORMATION
 - winnt/_HEAP_OPTIMIZE_RESOURCES_INFORMATION
 - PHEAP_OPTIMIZE_RESOURCES_INFORMATION
 - winnt/PHEAP_OPTIMIZE_RESOURCES_INFORMATION
 - HEAP_OPTIMIZE_RESOURCES_INFORMATION
 - winnt/HEAP_OPTIMIZE_RESOURCES_INFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - HEAP_OPTIMIZE_RESOURCES_INFORMATION
---

# HEAP_OPTIMIZE_RESOURCES_INFORMATION structure


## -description

Specifies  flags for a HeapOptimizeResources operation initiated with <a href="/windows/desktop/api/heapapi/nf-heapapi-heapsetinformation">HeapSetInformation</a>.

## -struct-fields

### -field Version

### -field Flags

## -remarks

Mandatory parameter to the HeapOptimizeResources class.

The <b>HEAP_OPTIMIZE_RESOURCES_CURRENT_VERSION</b> constant is available to fill in the Version field of the <b>HEAP_OPTIMIZE_RESOURCES_INFORMATION</b> structure. The only legal value for this field is currently 1.

## -see-also

<a href="/windows/desktop/Memory/memory-management-structures">Memory Management Structures</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-prefetchvirtualmemory">PrefetchVirtualMemory</a>