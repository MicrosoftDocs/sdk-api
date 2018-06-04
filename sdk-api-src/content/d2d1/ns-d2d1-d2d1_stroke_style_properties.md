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

# D2D1_STROKE_STYLE_PROPERTIES structure


## -description



Describes the stroke that outlines a shape.
	 	 


## -struct-fields




### -field startCap

Type: <b><a href="https://msdn.microsoft.com/acf4365e-b9df-459e-a746-016339cd09ac">D2D1_CAP_STYLE</a></b>

The cap applied to the start of all the open figures in a stroked geometry.


### -field endCap

Type: <b><a href="https://msdn.microsoft.com/acf4365e-b9df-459e-a746-016339cd09ac">D2D1_CAP_STYLE</a></b>

The cap applied to the end of all the open figures in a stroked geometry.


### -field dashCap

Type: <b><a href="https://msdn.microsoft.com/acf4365e-b9df-459e-a746-016339cd09ac">D2D1_CAP_STYLE</a></b>

The shape  at either end of each dash segment.


### -field lineJoin

Type: <b><a href="https://msdn.microsoft.com/4368e93e-af69-4555-ac2b-c9c576c81372">D2D1_LINE_JOIN</a></b>

A value that describes how segments are joined. This value is ignored for a vertex if the segment flags specify that the segment should have a smooth join. 


### -field miterLimit

Type: <b>FLOAT</b>

The limit of the thickness of the join on a mitered corner. This value is always treated as though it is greater than or equal to 1.0f.




### -field dashStyle

Type: <b><a href="https://msdn.microsoft.com/0c1807e3-51e6-440a-bd80-9b43ed7a39f5">D2D1_DASH_STYLE</a></b>

A value that specifies whether the stroke has a dash pattern and, if so, the dash style. 


### -field dashOffset

Type: <b>FLOAT</b>

A value that specifies an offset in the dash sequence.   A positive dash offset value  shifts the dash pattern, in units of  stroke width, toward the start of the stroked geometry.  A negative dash offset value  shifts the dash pattern, in units of  stroke width, toward the end of the stroked geometry.


## -remarks



The following illustration shows different <i>dashOffset</i> values for the same custom dash style.

<img alt="Illustration of four dashes with the same style and different dashOffset values" src="images/StrokeStyle_DashOffset.png"/>



