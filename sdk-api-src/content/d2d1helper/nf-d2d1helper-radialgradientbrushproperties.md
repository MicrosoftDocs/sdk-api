---
UID: NF:d2d1helper.RadialGradientBrushProperties
title: RadialGradientBrushProperties function
author: windows-sdk-content
description: Creates a D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES structure.
old-location: direct2d\radialgradientbrushproperties.htm
old-project: Direct2D
ms.assetid: d65ee26c-28d4-4b58-9089-1aab959246cc
ms.author: windowssdkdev
ms.date: 04/20/2018
ms.keywords: RadialGradientBrushProperties, RadialGradientBrushProperties function [Direct2D], d2d1helper/RadialGradientBrushProperties, direct2d.radialgradientbrushproperties
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: d2d1helper.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D2D1_VIGNETTE_PROP
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	D2d1.dll
api_name:
-	RadialGradientBrushProperties
product: Windows
targetos: Windows
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
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



