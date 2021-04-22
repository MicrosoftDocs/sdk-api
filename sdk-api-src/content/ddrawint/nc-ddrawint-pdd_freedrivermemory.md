---
UID: NC:ddrawint.PDD_FREEDRIVERMEMORY
title: PDD_FREEDRIVERMEMORY (ddrawint.h)
description: The DdFreeDriverMemory callback function frees offscreen or nonlocal display memory to satisfy a new allocation request.
helpviewer_keywords: ["DdFreeDriverMemory","DdFreeDriverMemory callback function [Display Devices]","PDD_FREEDRIVERMEMORY","PDD_FREEDRIVERMEMORY callback","ddfncs_cbc94a36-d6b1-45e5-925e-17738eae3904.xml","ddrawint/DdFreeDriverMemory","display.ddfreedrivermemory"]
old-location: display\ddfreedrivermemory.htm
tech.root: display
ms.assetid: dd37c6b5-2039-487f-badc-840ac6cc7906
ms.date: 12/05/2018
ms.keywords: DdFreeDriverMemory, DdFreeDriverMemory callback function [Display Devices], PDD_FREEDRIVERMEMORY, PDD_FREEDRIVERMEMORY callback, ddfncs_cbc94a36-d6b1-45e5-925e-17738eae3904.xml, ddrawint/DdFreeDriverMemory, display.ddfreedrivermemory
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PDD_FREEDRIVERMEMORY
 - ddrawint/PDD_FREEDRIVERMEMORY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ddrawint.h
api_name:
 - DdFreeDriverMemory
---


## -description

The <b>DdFreeDriverMemory</b> callback function frees offscreen or nonlocal display memory to satisfy a new allocation request.

## -parameters

### -param unnamedParam1


Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_freedrivermemorydata">DD_FREEDRIVERMEMORYDATA</a> structure that contains the details of the free request.

## -returns

<b>DdFreeDriverMemory</b> returns one of the following callback codes:

## -remarks

The driver should implement <b>DdFreeDriverMemory</b> when it has DirectDraw manage all offscreen display memory management, including allocations for <a href="/windows/desktop/api/winddi/nf-winddi-drvcreatedevicebitmap">DrvCreateDeviceBitmap</a>. DirectDraw requests for allocations in offscreen memory should always take precedence over GDI device bitmap allocations.

DirectDraw calls <b>DdFreeDriverMemory</b> when it does not have enough offscreen or nonlocal display memory to allocate a surface requested by an application. The driver should move a GDI device bitmap from offscreen memory into system memory and then immediately return. Bitmap moves can be accomplished by calling <a href="/windows/desktop/api/winddi/nf-winddi-engmodifysurface">EngModifySurface</a>.

DirectDraw will continually call <b>DdFreeDriverMemory</b> until there is enough offscreen memory from which to allocate the requested surface or until the driver returns DDERR_OUTOFMEMORY.

## -see-also

<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_freedrivermemorydata">DD_FREEDRIVERMEMORYDATA</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvcreatedevicebitmap">DrvCreateDeviceBitmap</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engmodifysurface">EngModifySurface</a>



<a href="/windows/desktop/api/dmemmgr/nf-dmemmgr-heapvidmemallocaligned">HeapVidMemAllocAligned</a>