---
UID: NC:avrfsdk.AVRF_HEAPALLOCATION_ENUMERATE_CALLBACK
title: AVRF_HEAPALLOCATION_ENUMERATE_CALLBACK (avrfsdk.h)
description: Receives information related to heap allocations.
helpviewer_keywords: ["AVRF_HEAPALLOCATION_ENUMERATE_CALLBACK","AVRF_HEAPALLOCATION_ENUMERATE_CALLBACK callback","AVRF_HEAPALLOCATION_ENUMERATE_CALLBACK callback function [Windows API]","avrfsdk/AVRF_HEAPALLOCATION_ENUMERATE_CALLBACK","base.avrf_heap_allocation_enumerate_callback","winprog.avrf_heap_allocation_enumerate_callback"]
old-location: winprog\avrf_heap_allocation_enumerate_callback.htm
tech.root: winprog
ms.assetid: 614d49f5-d119-4afe-b821-30ee9cb29582
ms.date: 12/05/2018
ms.keywords: AVRF_HEAPALLOCATION_ENUMERATE_CALLBACK, AVRF_HEAPALLOCATION_ENUMERATE_CALLBACK callback, AVRF_HEAPALLOCATION_ENUMERATE_CALLBACK callback function [Windows API], avrfsdk/AVRF_HEAPALLOCATION_ENUMERATE_CALLBACK, base.avrf_heap_allocation_enumerate_callback, winprog.avrf_heap_allocation_enumerate_callback
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AVRF_HEAPALLOCATION_ENUMERATE_CALLBACK
 - avrfsdk/AVRF_HEAPALLOCATION_ENUMERATE_CALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Avrfsdk.h
api_name:
 - AVRF_HEAPALLOCATION_ENUMERATE_CALLBACK
---

# AVRF_HEAPALLOCATION_ENUMERATE_CALLBACK callback function


## -description

Receives information related to heap allocations.

## -parameters

### -param HeapAllocation

A pointer to an <a href="/windows/desktop/api/avrfsdk/ns-avrfsdk-avrf_heap_allocation">AVRF_HEAP_ALLOCATION</a> structure containing information about the heap to be enumerated.

### -param EnumerationContext

A pointer to user-defined information in the context of the enumeration that is passed in when the <a href="/windows/desktop/api/avrfsdk/nf-avrfsdk-verifierenumerateresource">VerifierEnumerateResource</a> function is invoked.

### -param EnumerationLevel

A pointer to a value that informs the <a href="/windows/desktop/api/avrfsdk/nf-avrfsdk-verifierenumerateresource">VerifierEnumerateResource</a> function to either continue or stop the enumeration operation. These values are defined in the <a href="/windows/desktop/api/avrfsdk/ne-avrfsdk-eheapenumerationlevel">eHeapEnumerationLevel</a> enum.

## -returns

This function returns error codes or other values defined by the application.

## -see-also

<a href="/windows/desktop/DevNotes/resource-enumeration">Resource Enumeration</a>