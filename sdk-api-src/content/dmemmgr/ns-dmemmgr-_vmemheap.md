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

# _VMEMHEAP structure


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

