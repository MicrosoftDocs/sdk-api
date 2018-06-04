---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _AVRF_HEAP_ALLOCATION structure


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
 

 

