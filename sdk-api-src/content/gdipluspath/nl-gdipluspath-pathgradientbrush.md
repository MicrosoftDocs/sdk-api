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

# PathGradientBrush class


## -description


A <b>PathGradientBrush</b> object stores the attributes of a color gradient that you can use to fill the interior of a path with a gradually changing color. A path gradient brush has a boundary path, a boundary color, a center point, and a center color. When you paint an area with a path gradient brush, the color changes gradually from the boundary color to the center color as you move from the boundary path to the center point.


## -remarks



By default, the center point of a path gradient brush is the centroid of the boundary path, but you can set the center point to any location, inside or outside the path, by calling 
				<a href="https://msdn.microsoft.com/41765887-b1de-4259-95af-a1ef8c84d01a">PathGradientBrush::SetCenterPoint Methods</a>.

The boundary path can be a polygon specified by an array of points, and each of those points along the boundary can have a different color.

By default, the color is linearly related to the distance as you move from a point on the boundary to the center point. You can customize the relationship between color and distance by calling 
				<a href="https://msdn.microsoft.com/3abf3b42-d72e-413e-9daf-ba0e8146695e">PathGradientBrush::SetBlend</a>.



