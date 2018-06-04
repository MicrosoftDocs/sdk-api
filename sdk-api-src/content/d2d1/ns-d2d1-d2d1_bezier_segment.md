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

# D2D1_BEZIER_SEGMENT structure


## -description


Represents a cubic bezier segment drawn  between two points.


## -struct-fields




### -field point1

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The first control point for the Bezier segment.


### -field point2

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The second control point for the Bezier segment.


### -field point3

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The end point for the Bezier segment.


## -remarks




A cubic Bezier curve is defined by four points: a start point, an end point (<i>point3</i>), and two control points (<i>point1</i> and <i>point2</i>). A Bezier segment does not contain a property for the starting point of the curve; it defines only the end point. The beginning point of the curve is the current point of the path to which the Bezier curve is added.


The two control points of a cubic Bezier curve behave like magnets, attracting portions of what would otherwise be a straight line toward themselves and producing a curve. The first control point, <i>point1</i>, affects the beginning portion of the curve; the second control point, <i>point2</i>, affects the ending portion of the curve. 

<div class="alert"><b>Note</b>  The curve doesn't necessarily pass through either of the control points; each control point moves its portion of the line toward itself, but not through itself.</div>
<div> </div>


