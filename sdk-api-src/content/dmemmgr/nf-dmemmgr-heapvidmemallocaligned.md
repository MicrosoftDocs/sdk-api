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

# HeapVidMemAllocAligned function


## -description


The <b>HeapVidMemAllocAligned</b> function allocates <a href="https://msdn.microsoft.com/3f78ce93-03cd-45aa-9861-cdf6d557e6a5">off_screen_memory</a> for a display driver by using the DirectDraw video memory heap manager.


## -parameters




### -param lpVidMem [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff570171">VIDEOMEMORY</a> structure that represents the DirectDraw heap from which to allocate the surface.


### -param dwWidth [in]

Is the width in bytes of the requested surface.


### -param dwHeight [in]

Is the height in scan lines of the requested surface.


### -param lpAlignment [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569895">SURFACEALIGNMENT</a> structure that describes the alignment restrictions for the surface.


### -param lpNewPitch [out]

Is the location in which the resulting pitch value is written. This information is relevant only to linear (nonrectangular) off-screen heaps.


## -returns



<b>HeapVidMemAllocAligned</b> returns the FLATPTR offset of the resulting allocation upon success. Otherwise, it returns zero.




## -remarks



The driver should use the array of VIDEOMEMORY structures its <a href="https://msdn.microsoft.com/library/windows/hardware/ff556229">DrvGetDirectDrawInfo</a> function receives to determine the value of <i>lpVidMem</i> with which to call <b>HeapVidMemAllocAligned</b>. The driver receives this array in the <i>pvmList</i> parameter during the second call to <b>DrvGetDirectDrawInfo</b>. It is possible that <b>DrvGetDirectDrawInfo</b> might not be called when low memory conditions exist on the system. Consequently, the driver should always check to ensure that it has a non-NULL pointer in <i>pvmList</i>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556229">DrvGetDirectDrawInfo</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569895">SURFACEALIGNMENT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570171">VIDEOMEMORY</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570554">VidMemFree</a>
 

 

