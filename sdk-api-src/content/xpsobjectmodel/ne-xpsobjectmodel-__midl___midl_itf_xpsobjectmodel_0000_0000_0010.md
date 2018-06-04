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

# __MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0010 enumeration


## -description


The rule used by a composite shape to determine whether a given point is part of the geometry.


## -enum-fields




### -field XPS_FILL_RULE_EVENODD

The rule that determines whether a point is in the fill region. This is determined by drawing 
				a ray from the point to infinity in any direction, and counting the number 
				of path segments within the shape that the ray crosses. If this 
				number is odd, the point is inside; if even, the point is outside.


### -field XPS_FILL_RULE_NONZERO

The rule that determines whether a point is in the fill region of the 
				path. This is determined by drawing a ray from the point to infinity in any direction, and  
				examining the places where a segment of the shape crosses the ray. Start 
				the count at 0, then add 1 whenever a path segment crosses the ray from left 
				to right; subtract 1 whenever a path segment crosses the ray from 
				right to left. After the crossings are counted, 
				the point is outside the path if the result is zero and inside if otherwise.


## -see-also




<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

