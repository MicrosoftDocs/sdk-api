---
UID: NE:winnt._HEAP_INFORMATION_CLASS
title: HEAP_INFORMATION_CLASS (winnt.h)
description: Specifies the class of heap information to be set or retrieved.
helpviewer_keywords: ["HEAP_INFORMATION_CLASS","HEAP_INFORMATION_CLASS enumeration","HeapCompatibilityInformation","HeapEnableTerminationOnCorruption","base.heap_information_class","winnt/HEAP_INFORMATION_CLASS","winnt/HeapCompatibilityInformation","winnt/HeapEnableTerminationOnCorruption"]
old-location: base\heap_information_class.htm
tech.root: base
ms.assetid: 4D1B21D2-1F0E-4DC8-A583-220E9891DBBF
ms.date: 12/05/2018
ms.keywords: HEAP_INFORMATION_CLASS, HEAP_INFORMATION_CLASS enumeration, HeapCompatibilityInformation, HeapEnableTerminationOnCorruption, base.heap_information_class, winnt/HEAP_INFORMATION_CLASS, winnt/HeapCompatibilityInformation, winnt/HeapEnableTerminationOnCorruption
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: HEAP_INFORMATION_CLASS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HEAP_INFORMATION_CLASS
 - winnt/_HEAP_INFORMATION_CLASS
 - HEAP_INFORMATION_CLASS
 - winnt/HEAP_INFORMATION_CLASS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - HEAP_INFORMATION_CLASS
---

# HEAP_INFORMATION_CLASS enumeration


## -description

Specifies the class of heap information to be set or retrieved.

## -enum-fields

### -field HeapCompatibilityInformation:0

The heap features that are enabled. The available features vary based on operating system. Depending on the <i>HeapInformation</i> parameter in the <a href="/windows/desktop/api/heapapi/nf-heapapi-heapqueryinformation">HeapQueryInformation</a> or <a href="/windows/desktop/api/heapapi/nf-heapapi-heapsetinformation">HeapSetInformation</a> functions, specifying this enumeration value can indicate one of the following features:

<ul>
<li>A standard heap that does not support look-aside lists.</li>
<li>A heap that supports look-aside lists.</li>
<li>A <a href="/windows/desktop/Memory/low-fragmentation-heap">low-fragmentation heap</a> (LFH), which does not support look-aside lists.</li>
</ul>
For more information about look-aside lists, see the Remarks section.

### -field HeapEnableTerminationOnCorruption:1

The terminate-on-corruption feature. If the heap manager detects an error in any heap used by the 
         process, it calls the Windows Error Reporting service and terminates the process.

After a process enables this feature, it cannot be disabled.

### -field HeapOptimizeResources:3

## -remarks

To retrieve information about a heap, use the <a href="/windows/desktop/api/heapapi/nf-heapapi-heapqueryinformation">HeapQueryInformation</a> function. To enable features for a heap, use the 
<a href="/windows/desktop/api/heapapi/nf-heapapi-heapsetinformation">HeapSetInformation</a> function.

<b>Windows XP and Windows Server 2003:  </b> A look-aside list is a fast memory allocation mechanism that contains only fixed-sized blocks. Look-aside lists are enabled by default for heaps that support them. Starting with Windows Vista, look-aside lists are not used and the LFH is enabled by default.

Look-aside lists are faster than general pool allocations that vary in size, because the system does not search for free memory that fits the allocation. In addition, access to look-aside lists is generally synchronized using fast atomic processor exchange instructions instead of mutexes or spinlocks. Look-aside lists can be created by the system or drivers. They can be allocated from paged or nonpaged pool.

## -see-also

<a href="/windows/desktop/api/heapapi/nf-heapapi-heapqueryinformation">HeapQueryInformation</a>



<a href="/windows/desktop/api/heapapi/nf-heapapi-heapsetinformation">HeapSetInformation</a>
