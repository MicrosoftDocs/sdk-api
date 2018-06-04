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

# D2D1_STROKE_TRANSFORM_TYPE enumeration


## -description


Defines how the world transform, dots per inch (dpi), and stroke width affect the shape of the pen used to stroke a primitive.


## -enum-fields




### -field D2D1_STROKE_TRANSFORM_TYPE_NORMAL

The stroke respects the currently set world transform, the dpi, and the stroke width.


### -field D2D1_STROKE_TRANSFORM_TYPE_FIXED

The stroke does not respect the world transform but it does respect the dpi and stroke width.


### -field D2D1_STROKE_TRANSFORM_TYPE_HAIRLINE

The stroke is forced to 1 pixel wide (in device space) and does not respect the world transform, the dpi, or the stroke width.


### -field D2D1_STROKE_TRANSFORM_TYPE_FORCE_DWORD




## -remarks



If you specify <b>D2D1_STROKE_TRANSFORM_TYPE_FIXED</b> the stroke isn't affected by the world transform.

If you specify <b>D2D1_STROKE_TRANSFORM_TYPE_FIXED</b> the application has the same behavior in Windows 7 and later.

If you specify <b>D2D1_STROKE_TRANSFORM_TYPE_HAIRLINE</b> the stroke is always 1 pixel wide.

Apart from the stroke, any value derived from the stroke width is not affected when the transformType is either fixed or hairline. This includes miters, line caps and so on.

 

It is important to distinguish between the geometry being stroked and the shape of the stroke pen. When D2D1_STROKE_TRANSFORM_TYPE_FIXED or D2D1_STROKE_TRANSFORM_TYPE_HAIRLINE is specified, the geometry still respects the transform and dpi, but the pen that traces the geometry will not.

Here is an illustration of a stroke with dashing and a skew and stretch transform.

<img alt="An illustration of a stroke with dashing and a skew and stretch transform." src="images/skewedstroke.png"/>
And here is an illustration of a fixed width stroke which does not get transformed.

<img alt="An illustration of a fixed width stroke which does not get transformed." src="images/fixedwidthstroke.png"/>



## -see-also




<a href="https://msdn.microsoft.com/7afaa6f8-8e25-42ec-9afb-a5342bba11d0">ID2D1StrokeStyle1</a>
 

 

