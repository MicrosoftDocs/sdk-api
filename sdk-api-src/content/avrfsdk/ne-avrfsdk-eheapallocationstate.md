---
UID: NE:avrfsdk.eHeapAllocationState
title: eHeapAllocationState (avrfsdk.h)
description: Specifies the current heap allocation state.
helpviewer_keywords: ["HeapFullPageHeap","HeapMetadata","HeapStateMask","avrfsdk/HeapFullPageHeap","avrfsdk/HeapMetadata","avrfsdk/HeapStateMask","avrfsdk/eHeapAllocationState","base.eheapallocationstate","eHeapAllocationState","eHeapAllocationState enumeration [Windows API]","winprog.eheapallocationstate"]
old-location: winprog\eheapallocationstate.htm
tech.root: winprog
ms.assetid: c91b169d-fee5-46ad-a589-3b52436d779c
ms.date: 12/05/2018
ms.keywords: HeapFullPageHeap, HeapMetadata, HeapStateMask, avrfsdk/HeapFullPageHeap, avrfsdk/HeapMetadata, avrfsdk/HeapStateMask, avrfsdk/eHeapAllocationState, base.eheapallocationstate, eHeapAllocationState, eHeapAllocationState enumeration [Windows API], winprog.eheapallocationstate
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
 - eHeapAllocationState
 - avrfsdk/eHeapAllocationState
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
 - eHeapAllocationState
---

# eHeapAllocationState enumeration


## -description

Specifies the current heap allocation state.

## -enum-fields

### -field HeapFullPageHeap:0x40000000

Specifies the full-page heap arrangement is being used.

### -field HeapMetadata:0x80000000

Specifies the highest bit. When set, it has not been allocated by the user.

### -field HeapStateMask:0xFFFF0000

Specifies a value to be used as a mask with the bitwise AND operator to indicate whether the allocation is by the user.

## -see-also

<a href="/windows/desktop/DevNotes/resource-enumeration">Resource Enumeration</a>



<a href="/windows/desktop/api/avrfsdk/nf-avrfsdk-verifierenumerateresource">VerifierEnumerateResource</a>
