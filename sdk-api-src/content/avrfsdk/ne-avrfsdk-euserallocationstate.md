---
UID: NE:avrfsdk.eUserAllocationState
title: eUserAllocationState (avrfsdk.h)
description: Specifies the application's current heap allocation state.
helpviewer_keywords: ["AllocationStateBusy","AllocationStateFree","AllocationStateUnknown","avrfsdk/AllocationStateBusy","avrfsdk/AllocationStateFree","avrfsdk/AllocationStateUnknown","avrfsdk/eUserAllocationState","base.euserallocationstate","eUserAllocationState","eUserAllocationState enumeration [Windows API]","winprog.euserallocationstate"]
old-location: winprog\euserallocationstate.htm
tech.root: winprog
ms.assetid: 8aa46c8a-1261-47da-8145-e7ff9826d2ab
ms.date: 12/05/2018
ms.keywords: AllocationStateBusy, AllocationStateFree, AllocationStateUnknown, avrfsdk/AllocationStateBusy, avrfsdk/AllocationStateFree, avrfsdk/AllocationStateUnknown, avrfsdk/eUserAllocationState, base.euserallocationstate, eUserAllocationState, eUserAllocationState enumeration [Windows API], winprog.euserallocationstate
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
 - eUserAllocationState
 - avrfsdk/eUserAllocationState
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
 - eUserAllocationState
---

# eUserAllocationState enumeration


## -description

Specifies the application's current heap allocation state.

## -enum-fields

### -field AllocationStateUnknown

The allocation state cannot be determined.

### -field AllocationStateBusy

The allocation state is currently in use.

### -field AllocationStateFree

Memory has been freed from the stack but has not been returned to the heap yet.

## -see-also

<a href="/windows/desktop/DevNotes/resource-enumeration">Resource Enumeration</a>



<a href="/windows/desktop/api/avrfsdk/nf-avrfsdk-verifierenumerateresource">VerifierEnumerateResource</a>