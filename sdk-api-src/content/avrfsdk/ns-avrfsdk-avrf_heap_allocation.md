---
UID: NS:avrfsdk._AVRF_HEAP_ALLOCATION
title: AVRF_HEAP_ALLOCATION (avrfsdk.h)
author: windows-sdk-content
description: Stores metadata information about heap allocation.
old-location: winprog\avrf_heap_allocation.htm
tech.root: DevNotes
ms.assetid: 238c7de7-4bf1-4974-8a6f-09e4d5f756ab
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PAVRF_HEAP_ALLOCATION, AVRF_HEAP_ALLOCATION, AVRF_HEAP_ALLOCATION structure [Windows API], avrfsdk/AVRF_HEAP_ALLOCATION, base.avrf_heap_allocation, winprog.avrf_heap_allocation"
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Avrfsdk.h
api_name:
 - AVRF_HEAP_ALLOCATION
product: Windows
targetos: Windows
req.typenames: AVRF_HEAP_ALLOCATION, *PAVRF_HEAP_ALLOCATION
req.redist: 
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

One of the values in the <a href="https://msdn.microsoft.com/8aa46c8a-1261-47da-8145-e7ff9826d2ab">eUserAllocationState</a> enumerated type.


### -field HeapState

The state of the heap allocation. The user can extract one of the values in the <a href="https://msdn.microsoft.com/c91b169d-fee5-46ad-a589-3b52436d779c">eHeapAllocationState</a> enum after AND-ing the <b>HeapStateMask</b> value.


### -field HeapContext

The context of the heap currently allocated.


### -field BackTraceInformation

A pointer to an <a href="https://msdn.microsoft.com/634d9569-469c-4dc7-9192-217af0937b6c">AVRF_BACKTRACE_INFORMATION</a> structure containing information about the last operation that occurred on the allocation. 

When available, it can be the stack backtrace of the place where the address specified in the <b>UserAllocation</b> member of the structure was allocated (if <b>UserAllocationState</b> is <b>AllocationstateBusy</b>) or where the address specified in the <b>UserAllocation</b> member was freed (if <b>UserAllocationState</b> is <b>AllocationStateFree</b>).


## -see-also




<a href="https://msdn.microsoft.com/99cb9005-9cfc-44fb-b09f-fed0541cda37">Resource Enumeration</a>



<a href="https://msdn.microsoft.com/e1715f2a-5928-44e6-afbf-f2f0ab0ba3dd">VerifierEnumerateResource</a>
 

 

