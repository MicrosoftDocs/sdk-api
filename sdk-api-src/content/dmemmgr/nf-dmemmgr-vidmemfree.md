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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# VidMemFree function


## -description


The <b>VidMemFree</b> function frees <a href="https://msdn.microsoft.com/3f78ce93-03cd-45aa-9861-cdf6d557e6a5">off-screen memory</a> allocated for a display driver by <a href="https://msdn.microsoft.com/efd004d5-58fc-4721-9a74-d018cb3e5de9">HeapVidMemAllocAligned</a>.


## -parameters




### -param pvmh [in]

Pointer to a <a href="https://msdn.microsoft.com/bcc5eb95-a438-427f-bb16-7489e9485cd5">VMEMHEAP</a> structure that represents the DirectDraw heap from which the surface was allocated. The driver obtains this value from the <b>lpHeap</b> member of the <a href="https://msdn.microsoft.com/a472a9f6-d85e-429b-9b0d-efce576b6330">VIDEOMEMORY</a> structure originally passed to <b>HeapVidMemAllocAligned</b>.


### -param ptr [in]

Specifies the FLATPTR offset of the allocated surface. This data type is equivalent to a ULONG_PTR.


## -returns



None




## -see-also




<a href="https://msdn.microsoft.com/efd004d5-58fc-4721-9a74-d018cb3e5de9">HeapVidMemAllocAligned</a>



<a href="https://msdn.microsoft.com/a472a9f6-d85e-429b-9b0d-efce576b6330">VIDEOMEMORY</a>



<a href="https://msdn.microsoft.com/bcc5eb95-a438-427f-bb16-7489e9485cd5">VMEMHEAP</a>
 

 

