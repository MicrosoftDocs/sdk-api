---
UID: NS:avrfsdk._AVRF_HEAP_ALLOCATION
title: AVRF_HEAP_ALLOCATION (avrfsdk.h)
description: Stores metadata information about heap allocation.
helpviewer_keywords: ["*PAVRF_HEAP_ALLOCATION","AVRF_HEAP_ALLOCATION","AVRF_HEAP_ALLOCATION structure [Windows API]","avrfsdk/AVRF_HEAP_ALLOCATION","base.avrf_heap_allocation","winprog.avrf_heap_allocation"]
old-location: winprog\avrf_heap_allocation.htm
tech.root: winprog
ms.assetid: 238c7de7-4bf1-4974-8a6f-09e4d5f756ab
ms.date: 12/05/2018
ms.keywords: '*PAVRF_HEAP_ALLOCATION, AVRF_HEAP_ALLOCATION, AVRF_HEAP_ALLOCATION structure [Windows API], avrfsdk/AVRF_HEAP_ALLOCATION, base.avrf_heap_allocation, winprog.avrf_heap_allocation'
req.header: avrfsdk.h
req.include-header: 
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
req.typenames: AVRF_HEAP_ALLOCATION, *PAVRF_HEAP_ALLOCATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AVRF_HEAP_ALLOCATION
 - avrfsdk/_AVRF_HEAP_ALLOCATION
 - PAVRF_HEAP_ALLOCATION
 - avrfsdk/PAVRF_HEAP_ALLOCATION
 - AVRF_HEAP_ALLOCATION
 - avrfsdk/AVRF_HEAP_ALLOCATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Avrfsdk.h
api_name:
 - AVRF_HEAP_ALLOCATION
---

# AVRF_HEAP_ALLOCATION structure


## -description

Stores metadata information about heap allocation.

## -struct-fields

### -field HeapHandle

The handle to the heap being enumerated.

### -field UserAllocation

The address of the heap allocation as seen by the application.

### -field UserAllocationSize

The size, in bytes, of the application's allocation on the heap.

### -field Allocation

The address of the heap allocation as seen by the operating system.

### -field AllocationSize

The size, in bytes, of the heap allocation as seen by the operating system.

### -field UserAllocationState

One of the values in the <a href="/windows/desktop/api/avrfsdk/ne-avrfsdk-euserallocationstate">eUserAllocationState</a> enumerated type.

### -field HeapState

The state of the heap allocation. The user can extract one of the values in the <a href="/windows/desktop/api/avrfsdk/ne-avrfsdk-eheapallocationstate">eHeapAllocationState</a> enum after AND-ing the <b>HeapStateMask</b> value.

### -field HeapContext

The context of the heap currently allocated.

### -field BackTraceInformation

A pointer to an <a href="/windows/desktop/api/avrfsdk/ns-avrfsdk-avrf_backtrace_information">AVRF_BACKTRACE_INFORMATION</a> structure containing information about the last operation that occurred on the allocation. 

When available, it can be the stack backtrace of the place where the address specified in the <b>UserAllocation</b> member of the structure was allocated (if <b>UserAllocationState</b> is <b>AllocationstateBusy</b>) or where the address specified in the <b>UserAllocation</b> member was freed (if <b>UserAllocationState</b> is <b>AllocationStateFree</b>).

## -see-also

<a href="/windows/desktop/DevNotes/resource-enumeration">Resource Enumeration</a>



<a href="/windows/desktop/api/avrfsdk/nf-avrfsdk-verifierenumerateresource">VerifierEnumerateResource</a>