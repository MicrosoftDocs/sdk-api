---
UID: NS:dmemmgr._VMEMHEAP
title: VMEMHEAP (dmemmgr.h)
description: The VMEMHEAP structure contains information about the heap.
helpviewer_keywords: ["*LPVMEMHEAP","FAR *LPVMEMHEAP","FAR *LPVMEMHEAP structure [Display Devices]","VMEMHEAP","VMEMHEAP structure [Display Devices]","ddstrcts_3c571f23-5a4c-43c5-b7fb-69429f8c9dbe.xml","display.vmemheap","dmemmgr/FAR *LPVMEMHEAP","dmemmgr/VMEMHEAP"]
old-location: display\vmemheap.htm
tech.root: display
ms.assetid: bcc5eb95-a438-427f-bb16-7489e9485cd5
ms.date: 12/05/2018
ms.keywords: '*LPVMEMHEAP, FAR *LPVMEMHEAP, FAR *LPVMEMHEAP structure [Display Devices], VMEMHEAP, VMEMHEAP structure [Display Devices], ddstrcts_3c571f23-5a4c-43c5-b7fb-69429f8c9dbe.xml, display.vmemheap, dmemmgr/FAR *LPVMEMHEAP, dmemmgr/VMEMHEAP'
req.header: dmemmgr.h
req.include-header: Dmemmgr.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: VMEMHEAP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VMEMHEAP
 - dmemmgr/_VMEMHEAP
 - VMEMHEAP
 - dmemmgr/VMEMHEAP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dmemmgr.h
api_name:
 - VMEMHEAP
---

# VMEMHEAP structure


## -description

The VMEMHEAP structure contains information about the heap.

## -struct-fields

### -field dwFlags

Reserved for system use and should be ignored by the driver.

### -field stride

Reserved for system use and should be ignored by the driver.

### -field freeList

Reserved for system use and should be ignored by the driver.

### -field allocList

Reserved for system use and should be ignored by the driver.

### -field dwTotalSize

Reserved for system use and should be ignored by the driver.

### -field fpGARTLin

Points to the linear graphic address remapping table (GART) address of the start of the heap for nonlocal display memory.

### -field fpGARTDev

Points to the physical GART address of the start of the heap for nonlocal display memory.

### -field dwCommitedSize

Reserved for system use and should be ignored by the driver.

### -field dwCoalesceCount

Reserved for system use and should be ignored by the driver.

### -field Alignment

Reserved for system use and should be ignored by the driver.

### -field ddsCapsExAlt

Reserved for system use and should be ignored by the driver.

### -field ddsCapsEx

Reserved for system use and should be ignored by the driver.

### -field liPhysAGPBase

Reserved for system use and should be ignored by the driver.

### -field hdevAGP

Reserved for system use and should be ignored by the driver.

### -field pvPhysRsrv

Reserved for system use and should be ignored by the driver.

### -field pAgpCommitMask

Reserved for system use and should be ignored by the driver.

### -field dwAgpCommitMaskSize

Reserved for system use and should be ignored by the driver.

