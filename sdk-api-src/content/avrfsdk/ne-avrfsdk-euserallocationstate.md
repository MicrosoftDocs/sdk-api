---
UID: NE:avrfsdk.eUserAllocationState
title: eUserAllocationState
author: windows-driver-content
description: Specifies the application's current heap allocation state.
old-location: winprog\euserallocationstate.htm
old-project: DevNotes
ms.assetid: 8aa46c8a-1261-47da-8145-e7ff9826d2ab
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: AllocationStateBusy, AllocationStateFree, AllocationStateUnknown, avrfsdk/AllocationStateBusy, avrfsdk/AllocationStateFree, avrfsdk/AllocationStateUnknown, avrfsdk/eUserAllocationState, base.euserallocationstate, eUserAllocationState, eUserAllocationState enumeration [Windows API], winprog.euserallocationstate
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Avrfsdk.h
api_name:
-	eUserAllocationState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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




<a href="https://msdn.microsoft.com/99cb9005-9cfc-44fb-b09f-fed0541cda37">Resource Enumeration</a>



<a href="https://msdn.microsoft.com/e1715f2a-5928-44e6-afbf-f2f0ab0ba3dd">VerifierEnumerateResource</a>
 

 

