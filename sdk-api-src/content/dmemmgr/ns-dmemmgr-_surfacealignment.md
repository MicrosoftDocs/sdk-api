---
UID: NS:dmemmgr._SURFACEALIGNMENT
title: "_SURFACEALIGNMENT"
author: windows-sdk-content
description: The SURFACEALIGNMENT structure is used by a display driver to describe the alignment restrictions for a surface being allocated by HeapVidMemAllocAligned.
old-location: display\surfacealignment.htm
tech.root: display
ms.assetid: 200f4e08-b5d3-484e-b87a-b3069dc3c99f
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: "*LPSURFACEALIGNMENT, SURFACEALIGNMENT, SURFACEALIGNMENT structure [Display Devices], _SURFACEALIGNMENT, display.surfacealignment, dmemmgr/SURFACEALIGNMENT, grstrcts_8ab8c373-9600-45dc-9f16-f6c4de52a0c7.xml"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: dmemmgr.h
req.include-header: Winddi.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dmemmgr.h
api_name:
 - SURFACEALIGNMENT
product: Windows
targetos: Windows
req.typenames: SURFACEALIGNMENT, *LPSURFACEALIGNMENT
req.redist: 
---

# _SURFACEALIGNMENT structure


## -description


The SURFACEALIGNMENT structure is used by a display driver to describe the alignment restrictions for a surface being allocated by <a href="https://msdn.microsoft.com/efd004d5-58fc-4721-9a74-d018cb3e5de9">HeapVidMemAllocAligned</a>.


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




<a href="https://msdn.microsoft.com/efd004d5-58fc-4721-9a74-d018cb3e5de9">HeapVidMemAllocAligned</a>
 

 

