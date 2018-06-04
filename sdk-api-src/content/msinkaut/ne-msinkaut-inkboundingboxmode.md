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

# InkBoundingBoxMode enumeration


## -description



Specifies which characteristics of a stroke, such as drawing attributes, are used to calculate the bounding box of the ink.

The bounding box is the smallest rectangle that includes all points in the <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object. The size of the rectangle varies depending on whether you use drawing attributes, Bezier curve fitting, or just the points of the stroke to calculate the rectangle.




## -enum-fields




### -field IBBM_Default

 The definition of each stroke (polyline or Bezier) is used to calculate the bounding box; includes the drawing attributes, such as pen width, in the calculation.


### -field IBBM_NoCurveFit

 The polyline of the strokes (ignoring Bezier curve fitting requests) is used to calculate the bounding box; includes the drawing attributes in the calculation.


### -field IBBM_CurveFit

The  Bezier curve fitting line of the strokes (apply Bezier curve fitting to all strokes) is used to calculate the bounding box; includes the drawing attributes in the calculation.


### -field IBBM_PointsOnly

 Only the points of the strokes are used to calculate the bounding box.


### -field IBBM_Union

 The union of a NoCurveFit request and a CurveFit request.


## -see-also




<a href="https://msdn.microsoft.com/3b2c8cfc-05e6-4b53-b709-72291ee78471">GetBoundingBox Method</a>



<a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp Class</a>
 

 

