---
UID: NF:dmemmgr.VidMemFree
title: VidMemFree function
author: windows-driver-content
description: The VidMemFree function frees off-screen memory allocated for a display driver by HeapVidMemAllocAligned.
old-location: display\vidmemfree.htm
old-project: display
ms.assetid: f1d3b5a0-f1e3-4977-8081-839b4e36971f
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: VidMemFree, VidMemFree function [Display Devices], display.vidmemfree, dmemmgr/VidMemFree, gdifncs_a3a43790-1189-4c79-965c-aa20f04c7405.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Win32k.sys
api_name:
-	VidMemFree
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
---

# VidMemFree function


## -description


The <b>VidMemFree</b> function frees <a href="https://msdn.microsoft.com/3f78ce93-03cd-45aa-9861-cdf6d557e6a5">off-screen memory</a> allocated for a display driver by <a href="https://msdn.microsoft.com/library/windows/hardware/ff567267">HeapVidMemAllocAligned</a>.


## -parameters




### -param pvmh [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff570561">VMEMHEAP</a> structure that represents the DirectDraw heap from which the surface was allocated. The driver obtains this value from the <b>lpHeap</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff570171">VIDEOMEMORY</a> structure originally passed to <b>HeapVidMemAllocAligned</b>.


### -param ptr [in]

Specifies the FLATPTR offset of the allocated surface. This data type is equivalent to a ULONG_PTR.


## -returns



None




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff567267">HeapVidMemAllocAligned</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570171">VIDEOMEMORY</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570561">VMEMHEAP</a>
 

 

