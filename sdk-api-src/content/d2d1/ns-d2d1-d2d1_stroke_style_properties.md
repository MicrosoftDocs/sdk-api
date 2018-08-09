---
UID: NS:d2d1.D2D1_STROKE_STYLE_PROPERTIES
title: D2D1_STROKE_STYLE_PROPERTIES
author: windows-sdk-content
description: Describes the stroke that outlines a shape.
old-location: direct2d\D2D1_STROKE_STYLE_PROPERTIES.htm
old-project: direct2d
ms.assetid: 67f3701f-febd-4afe-803e-c5d9dbcd1b21
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: D2D1_STROKE_STYLE_PROPERTIES, D2D1_STROKE_STYLE_PROPERTIES structure [Direct2D], d2d1/D2D1_STROKE_STYLE_PROPERTIES, direct2d.D2D1_STROKE_STYLE_PROPERTIES
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: D2D1_STROKE_STYLE_PROPERTIES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1.h
api_name:
 - D2D1_STROKE_STYLE_PROPERTIES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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

<img alt="Illustration of four dashes with the same style and different dashOffset values" src="./images/StrokeStyle_DashOffset.png"/>



