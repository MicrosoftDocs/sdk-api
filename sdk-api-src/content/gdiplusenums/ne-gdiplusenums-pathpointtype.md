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

# PathPointType enumeration


## -description


The <b>PathPointType</b> enumeration indicates point types and flags for the data points in a path. Bits 0 through 2 indicate the type of a point, and bits 3 through 7 hold a set of flags that specify attributes of a point. This enumeration is used by the <a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a>, <a href="https://msdn.microsoft.com/f534b1b2-1fe3-4f30-8a7f-30d44f11d297">GraphicsPathIterator</a>, and <a href="https://msdn.microsoft.com/library/windows/hardware/ff568848">PathData</a> classes.


## -enum-fields




### -field PathPointTypeStart

Indicates that the point is the start of a figure. 


### -field PathPointTypeLine

Indicates that the point is one of the two endpoints of a line. 


### -field PathPointTypeBezier

Indicates that the point is an endpoint or control point of a cubic Bézier spline. 


### -field PathPointTypePathTypeMask

Masks all bits except for the three low-order bits, which indicate the point type. 


### -field PathPointTypeDashMode


### -field PathPointTypePathMarker

Specifies that the point is a marker. 


### -field PathPointTypeCloseSubpath

Specifies that the point is the last point in a closed subpath (figure). 


### -field PathPointTypeBezier3

Indicates that the point is an endpoint or control point of a cubic Bézier spline. 


#### - PathPointTypePathDashMode

Not used. 


## -remarks



A <a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a> object has an array of points and an array of types. Each element in the array of types is a byte that specifies the point type and a set of flags for the corresponding element in the array of points.




## -see-also




<a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a>



<a href="https://msdn.microsoft.com/f534b1b2-1fe3-4f30-8a7f-30d44f11d297">GraphicsPathIterator</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568848">PathData</a>
 

 

