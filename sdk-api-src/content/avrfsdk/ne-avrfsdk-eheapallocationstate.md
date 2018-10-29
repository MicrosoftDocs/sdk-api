---
UID: NE:avrfsdk.eHeapAllocationState
title: eHeapAllocationState
author: windows-sdk-content
description: Specifies the current heap allocation state.
old-location: winprog\eheapallocationstate.htm
tech.root: DevNotes
ms.assetid: c91b169d-fee5-46ad-a589-3b52436d779c
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: HeapFullPageHeap, HeapMetadata, HeapStateMask, avrfsdk/HeapFullPageHeap, avrfsdk/HeapMetadata, avrfsdk/HeapStateMask, avrfsdk/eHeapAllocationState, base.eheapallocationstate, eHeapAllocationState, eHeapAllocationState enumeration [Windows API], winprog.eheapallocationstate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
 - eHeapAllocationState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# eHeapAllocationState enumeration


## -description


Specifies the current heap allocation state.


## -enum-fields




### -field HeapFullPageHeap

Specifies the full-page heap arrangement is being used.


### -field HeapMetadata

Specifies the highest bit. When set, it has not been allocated by the user.


### -field HeapStateMask

Specifies a value to be used as a mask with the bitwise AND operator to indicate whether the allocation is by the user.


## -see-also




<a href="https://msdn.microsoft.com/99cb9005-9cfc-44fb-b09f-fed0541cda37">Resource Enumeration</a>



<a href="https://msdn.microsoft.com/e1715f2a-5928-44e6-afbf-f2f0ab0ba3dd">VerifierEnumerateResource</a>
 

 

