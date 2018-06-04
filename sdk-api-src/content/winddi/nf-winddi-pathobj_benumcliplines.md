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

# PATHOBJ_bEnumClipLines function


## -description


The <b>PATHOBJ_bEnumClipLines</b> function enumerates clipped line segments from a given path. 


## -parameters




### -param ppo

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff568849">PATHOBJ</a> structure containing the clipped line segments that are to be enumerated.


### -param cb

Specifies the size of the output buffer, in bytes. GDI does not write beyond this point in the buffer. The value of this parameter must be large enough to hold a <a href="https://msdn.microsoft.com/library/windows/hardware/ff539416">CLIPLINE</a> structure with at least one <a href="https://msdn.microsoft.com/library/windows/hardware/ff569516">RUN</a> structure. The driver should allocate space for several RUN structures.


### -param pcl

Pointer to the buffer that receives a CLIPLINE structure. The structure contains the original unclipped control points for a line segment. (The correct pixels for the line cannot be computed without the original points.) RUN structures, which describe sets of pixels along the line that are not clipped away, are written to this buffer.

If a clip region is complex, a single line segment can be broken into many RUN structures. A segment is returned as many times as necessary to list all of its RUN structures.

The CLIPLINE structure contains the starting and ending points of the original unclipped line and the line segments, or RUN structures, of that line that are to appear on the display.


## -returns



The return value is <b>TRUE</b> if more line segments are to be enumerated, indicating that this service should be called again. Otherwise, it is <b>FALSE</b>, indicating that the returned segment is the last segment in the path.




## -remarks



The enumeration must be started with <a href="https://msdn.microsoft.com/library/windows/hardware/ff568857">PATHOBJ_vEnumStartClipLines</a> before the driver makes this call.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff539416">CLIPLINE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568849">PATHOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568857">PATHOBJ_vEnumStartClipLines</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569516">RUN</a>
 

 

