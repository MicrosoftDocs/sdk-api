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
 

 

