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

# D2D1_POINT_DESCRIPTION structure


## -description


Describes a point on a path geometry.


## -struct-fields




### -field point

The end point after walking the path.


### -field unitTangentVector

A unit vector indicating the tangent point.


### -field endSegment

The index of the segment on which point resides. This index is global to the entire path, not just to a particular figure.


### -field endFigure

The index of the figure on which point resides.


### -field lengthToEndSegment

The length of the section of the path stretching from the start of the path  to the start of <b>endSegment</b>.


## -see-also




<a href="https://msdn.microsoft.com/4a47d928-7482-413a-ad9d-e887b309e367">ID2D1PathGeometry1::ComputePointAndSegmentAtLength</a>
 

 

