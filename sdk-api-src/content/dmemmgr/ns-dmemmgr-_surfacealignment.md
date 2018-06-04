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

# _SURFACEALIGNMENT structure


## -description


The SURFACEALIGNMENT structure is used by a display driver to describe the alignment restrictions for a surface being allocated by <a href="https://msdn.microsoft.com/library/windows/hardware/ff567267">HeapVidMemAllocAligned</a>.


## -struct-fields




### -field Linear

Is a structure that describes the alignment restrictions for linear heap allocations. 


### -field Linear.dwStartAlignment

Is the start alignment multiple in bytes that DirectDraw should respect when performing linear heap allocations. The driver should set this member to zero if no particular alignment is required.


### -field Linear.dwPitchAlignment

Is the end alignment multiple in bytes that DirectDraw should respect when performing linear heap allocations. The driver should set this member to zero if no particular alignment is required.


### -field Linear.dwFlags

Is reserved for system use and should be ignored by the display driver.


### -field Linear.dwReserved2

Is reserved for system use and should be ignored by the display driver.


### -field Rectangular

Is a structure that describes the alignment restrictions for rectangular heap allocations.


### -field Rectangular.dwXAlignment

Is the X alignment multiple in bytes that DirectDraw should respect when performing rectangular heap allocations. The driver cannot specify an X alignment that is more fine-grained than one doubleword; DirectDraw will round any X alignment up to the nearest multiple of 4 bytes. The driver should set this member to zero if no particular alignment is required.


### -field Rectangular.dwYAlignment

Is the Y alignment multiple in bytes that DirectDraw should respect when performing rectangular heap allocations. The driver should set this member to zero if no particular alignment is required.


### -field Rectangular.dwFlags

Is reserved for system use and should be ignored by the display driver.


### -field Rectangular.dwReserved2

Is reserved for system use and should be ignored by the display driver.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff567267">HeapVidMemAllocAligned</a>
 

 

