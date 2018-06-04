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

# EqualRect function


## -description


The <b>EqualRect</b> function determines whether the two specified rectangles are equal by comparing the coordinates of their upper-left and lower-right corners.


## -parameters




### -param lprc1 [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that contains the logical coordinates of the first rectangle.


### -param lprc2 [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that contains the logical coordinates of the second rectangle.


## -returns



If the two rectangles are identical, the return value is nonzero.

If the two rectangles are not identical, the return value is zero.




## -remarks



The <b>EqualRect</b> function does not treat empty rectangles as equal if their coordinates are different.

Because applications can use rectangles for different purposes, the rectangle functions do not use an explicit unit of measure. Instead, all rectangle coordinates and dimensions are given in signed, logical values. The mapping mode and the function in which the rectangle is used determine the units of measure.




## -see-also




<a href="https://msdn.microsoft.com/9deeed4f-304e-47a3-8259-ed7bc3815fd7">IsRectEmpty</a>



<a href="https://msdn.microsoft.com/8a47a238-082c-44b8-a270-5ebb4d3d9fc8">PtInRect</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>



<a href="https://msdn.microsoft.com/b03da8c9-ee6d-4045-8d90-8beceb09ead5">Rectangle Functions</a>



<a href="https://msdn.microsoft.com/23c251d1-b8c5-425f-b2b3-44954cf653e9">Rectangles Overview</a>
 

 

