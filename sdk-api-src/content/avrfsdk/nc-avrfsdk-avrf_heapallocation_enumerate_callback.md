---
UID: NC:avrfsdk.AVRF_HEAPALLOCATION_ENUMERATE_CALLBACK
title: AVRF_HEAPALLOCATION_ENUMERATE_CALLBACK
author: windows-sdk-content
description: Receives information related to heap allocations.
old-location: winprog\avrf_heap_allocation_enumerate_callback.htm
tech.root: DevNotes
ms.assetid: 614d49f5-d119-4afe-b821-30ee9cb29582
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: AVRF_HEAPALLOCATION_ENUMERATE_CALLBACK, AVRF_HEAPALLOCATION_ENUMERATE_CALLBACK callback, AVRF_HEAPALLOCATION_ENUMERATE_CALLBACK callback function [Windows API], avrfsdk/AVRF_HEAPALLOCATION_ENUMERATE_CALLBACK, base.avrf_heap_allocation_enumerate_callback, winprog.avrf_heap_allocation_enumerate_callback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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
 - UserDefined
api_location:
 - Avrfsdk.h
api_name:
 - AVRF_HEAPALLOCATION_ENUMERATE_CALLBACK
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AVRF_HEAPALLOCATION_ENUMERATE_CALLBACK callback function


## -description


Receives information related to heap allocations.


## -parameters




### -param HeapAllocation

A pointer to an <a href="https://msdn.microsoft.com/238c7de7-4bf1-4974-8a6f-09e4d5f756ab">AVRF_HEAP_ALLOCATION</a> structure containing information about the heap to be enumerated.


### -param EnumerationContext

A pointer to user-defined information in the context of the enumeration that is passed in when the <a href="https://msdn.microsoft.com/e1715f2a-5928-44e6-afbf-f2f0ab0ba3dd">VerifierEnumerateResource</a> function is invoked.


### -param EnumerationLevel

A pointer to a value that informs the <a href="https://msdn.microsoft.com/e1715f2a-5928-44e6-afbf-f2f0ab0ba3dd">VerifierEnumerateResource</a> function to either continue or stop the enumeration operation. These values are defined in the <a href="https://msdn.microsoft.com/f8260ae8-eb1e-45f4-babc-905f4af7e3b1">eHeapEnumerationLevel</a> enum.


## -returns



This function returns error codes or other values defined by the application.




## -see-also




<a href="https://msdn.microsoft.com/99cb9005-9cfc-44fb-b09f-fed0541cda37">Resource Enumeration</a>
 

 

