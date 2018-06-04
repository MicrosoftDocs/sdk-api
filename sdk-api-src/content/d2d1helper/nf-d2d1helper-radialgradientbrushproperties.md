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

# RadialGradientBrushProperties function


## -description


Creates a <a href="https://msdn.microsoft.com/194f7624-ac3b-4054-8d6f-5b4c99ef6546">D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES</a> structure.


## -parameters




### -param center [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

In the brush's coordinate space, the center of the gradient ellipse.


### -param gradientOriginOffset [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

In the brush's coordinate space, the offset of the gradient origin relative to the gradient ellipse's center.


### -param radiusX [in]

Type: <b>const FLOAT</b>

In the brush's coordinate space, the x-radius of the gradient ellipse.


### -param radiusY [in]

Type: <b>const FLOAT</b>

In the brush's coordinate space, the y-radius of the gradient ellipse.


## -returns



Type: <b><a href="https://msdn.microsoft.com/194f7624-ac3b-4054-8d6f-5b4c99ef6546">D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES</a></b>

A structure that contains the gradient origin offset and the size and position of the gradient ellipse for an <a href="https://msdn.microsoft.com/21ed2286-e4df-4b77-ba31-e5d5927e16f5">ID2D1RadialGradientBrush</a>.



