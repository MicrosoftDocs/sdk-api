---
UID: NF:dmemmgr.VidMemFree
title: VidMemFree function (dmemmgr.h)
author: windows-sdk-content
description: The VidMemFree function frees off-screen memory allocated for a display driver by HeapVidMemAllocAligned.
old-location: display\vidmemfree.htm
tech.root: display
ms.assetid: f1d3b5a0-f1e3-4977-8081-839b4e36971f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: VidMemFree, VidMemFree function [Display Devices], display.vidmemfree, dmemmgr/VidMemFree, gdifncs_a3a43790-1189-4c79-965c-aa20f04c7405.xml
ms.topic: function
f1_keywords:
- dmemmgr/VidMemFree
req.header: dmemmgr.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Win32k.sys
api_name:
- VidMemFree
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# VidMemFree function


## -description


The <b>VidMemFree</b> function frees <a href="https://docs.microsoft.com/windows-hardware/drivers/">off-screen memory</a> allocated for a display driver by <a href="https://docs.microsoft.com/windows/desktop/api/dmemmgr/nf-dmemmgr-heapvidmemallocaligned">HeapVidMemAllocAligned</a>.


## -parameters




### -param pvmh [in]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/dmemmgr/ns-dmemmgr-vmemheap">VMEMHEAP</a> structure that represents the DirectDraw heap from which the surface was allocated. The driver obtains this value from the <b>lpHeap</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/ns-ddrawint-videomemory">VIDEOMEMORY</a> structure originally passed to <b>HeapVidMemAllocAligned</b>.


### -param ptr [in]

Specifies the FLATPTR offset of the allocated surface. This data type is equivalent to a ULONG_PTR.


## -returns



None




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dmemmgr/nf-dmemmgr-heapvidmemallocaligned">HeapVidMemAllocAligned</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/ns-ddrawint-videomemory">VIDEOMEMORY</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dmemmgr/ns-dmemmgr-vmemheap">VMEMHEAP</a>
 

 

