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

# PDD_FREEDRIVERMEMORY callback function


## -description


The <b>DdFreeDriverMemory</b> callback function frees offscreen or nonlocal display memory to satisfy a new allocation request.


## -parameters




### -param Arg1








#### - lpfdm

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551524">DD_FREEDRIVERMEMORYDATA</a> structure that contains the details of the free request.


## -returns



<b>DdFreeDriverMemory</b> returns one of the following callback codes:




## -remarks



The driver should implement <b>DdFreeDriverMemory</b> when it has DirectDraw manage all offscreen display memory management, including allocations for <a href="https://msdn.microsoft.com/library/windows/hardware/ff556185">DrvCreateDeviceBitmap</a>. DirectDraw requests for allocations in offscreen memory should always take precedence over GDI device bitmap allocations.

DirectDraw calls <b>DdFreeDriverMemory</b> when it does not have enough offscreen or nonlocal display memory to allocate a surface requested by an application. The driver should move a GDI device bitmap from offscreen memory into system memory and then immediately return. Bitmap moves can be accomplished by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff564976">EngModifySurface</a>.

DirectDraw will continually call <b>DdFreeDriverMemory</b> until there is enough offscreen memory from which to allocate the requested surface or until the driver returns DDERR_OUTOFMEMORY.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551524">DD_FREEDRIVERMEMORYDATA</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556185">DrvCreateDeviceBitmap</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564976">EngModifySurface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff567267">HeapVidMemAllocAligned</a>
 

 

