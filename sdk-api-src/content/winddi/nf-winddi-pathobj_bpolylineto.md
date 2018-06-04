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

# PATHOBJ_bPolyLineTo function


## -description


The <b>PATHOBJ_bPolyLineTo</b> function draws lines from the current position in a path through the specified points.


## -parameters




### -param ppo

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff568849">PATHOBJ</a> structure created by the driver.


### -param pptfx

Pointer to an array of POINTFIX structures that define control points. The first line is drawn from the current position to the first point in this array; lines are then drawn to each subsequent point in the array. For a description of this data type, see <a href="https://msdn.microsoft.com/2054aa16-6d86-4db3-8b16-4570b0374e23">GDI Data Types</a>.


### -param cptfx

Specifies the count of points in <i>pptfx</i>. This is also the number of lines that will be added to the path.


## -returns



The return value is <b>TRUE</b> if the function is successful. Otherwise, it is <b>FALSE</b>, and an error code is logged.




## -remarks



<b>PATHOBJ_bPolyLineTo</b> should only be called with PATHOBJ structures created by <a href="https://msdn.microsoft.com/library/windows/hardware/ff564755">EngCreatePath</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564755">EngCreatePath</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568849">PATHOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568854">PATHOBJ_bPolyBezierTo</a>
 

 

