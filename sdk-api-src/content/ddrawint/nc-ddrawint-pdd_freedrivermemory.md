---
UID: NC:ddrawint.PDD_FREEDRIVERMEMORY
title: PDD_FREEDRIVERMEMORY
author: windows-sdk-content
description: The DdFreeDriverMemory callback function frees offscreen or nonlocal display memory to satisfy a new allocation request.
old-location: display\ddfreedrivermemory.htm
tech.root: display
ms.assetid: dd37c6b5-2039-487f-badc-840ac6cc7906
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: DdFreeDriverMemory, DdFreeDriverMemory callback function [Display Devices], PDD_FREEDRIVERMEMORY, PDD_FREEDRIVERMEMORY callback, ddfncs_cbc94a36-d6b1-45e5-925e-17738eae3904.xml, ddrawint/DdFreeDriverMemory, display.ddfreedrivermemory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: ddrawint.h
req.include-header: Winddi.h
req.target-type: Desktop
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
 - UserDefined
api_location:
 - ddrawint.h
api_name:
 - DdFreeDriverMemory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PDD_FREEDRIVERMEMORY callback function


## -description


The <b>DdFreeDriverMemory</b> callback function frees offscreen or nonlocal display memory to satisfy a new allocation request.


## -parameters




### -param Arg1








#### - lpfdm

Points to a <a href="https://msdn.microsoft.com/48a42f19-bb4f-4325-b68b-91f59a674771">DD_FREEDRIVERMEMORYDATA</a> structure that contains the details of the free request.


## -returns



<b>DdFreeDriverMemory</b> returns one of the following callback codes:




## -remarks



The driver should implement <b>DdFreeDriverMemory</b> when it has DirectDraw manage all offscreen display memory management, including allocations for <a href="https://msdn.microsoft.com/1f5f49ef-bf08-4311-9a1b-fdc37e6c2063">DrvCreateDeviceBitmap</a>. DirectDraw requests for allocations in offscreen memory should always take precedence over GDI device bitmap allocations.

DirectDraw calls <b>DdFreeDriverMemory</b> when it does not have enough offscreen or nonlocal display memory to allocate a surface requested by an application. The driver should move a GDI device bitmap from offscreen memory into system memory and then immediately return. Bitmap moves can be accomplished by calling <a href="https://msdn.microsoft.com/176f51c0-0075-4afb-8b5c-5d0b6b64a3ad">EngModifySurface</a>.

DirectDraw will continually call <b>DdFreeDriverMemory</b> until there is enough offscreen memory from which to allocate the requested surface or until the driver returns DDERR_OUTOFMEMORY.




## -see-also




<a href="https://msdn.microsoft.com/48a42f19-bb4f-4325-b68b-91f59a674771">DD_FREEDRIVERMEMORYDATA</a>



<a href="https://msdn.microsoft.com/1f5f49ef-bf08-4311-9a1b-fdc37e6c2063">DrvCreateDeviceBitmap</a>



<a href="https://msdn.microsoft.com/176f51c0-0075-4afb-8b5c-5d0b6b64a3ad">EngModifySurface</a>



<a href="https://msdn.microsoft.com/efd004d5-58fc-4721-9a74-d018cb3e5de9">HeapVidMemAllocAligned</a>
 

 

