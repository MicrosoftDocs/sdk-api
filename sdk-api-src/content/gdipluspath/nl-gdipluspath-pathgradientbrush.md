---
UID: NL:gdipluspath.PathGradientBrush
title: PathGradientBrush
author: windows-sdk-content
description: A PathGradientBrush object stores the attributes of a color gradient that you can use to fill the interior of a path with a gradually changing color.
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrush.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: PathGradientBrush, PathGradientBrush class [GDI+], PathGradientBrush class [GDI+],described, _gdiplus_CLASS_PathGradientBrush_Class, gdiplus._gdiplus_CLASS_PathGradientBrush_Class, gdipluspath/PathGradientBrush
ms.prod: windows
ms.technology: windows-sdk
ms.topic: class
req.header: gdipluspath.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - gdipluspath.h
api_name:
 - PathGradientBrush
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PathGradientBrush class


## -description


A <b>PathGradientBrush</b> object stores the attributes of a color gradient that you can use to fill the interior of a path with a gradually changing color. A path gradient brush has a boundary path, a boundary color, a center point, and a center color. When you paint an area with a path gradient brush, the color changes gradually from the boundary color to the center color as you move from the boundary path to the center point.


## -remarks



By default, the center point of a path gradient brush is the centroid of the boundary path, but you can set the center point to any location, inside or outside the path, by calling 
				<a href="https://msdn.microsoft.com/en-us/library/ms535078(v=VS.85).aspx">PathGradientBrush::SetCenterPoint Methods</a>.

The boundary path can be a polygon specified by an array of points, and each of those points along the boundary can have a different color.

By default, the color is linearly related to the distance as you move from a point on the boundary to the center point. You can customize the relationship between color and distance by calling 
				<a href="https://msdn.microsoft.com/en-us/library/ms535084(v=VS.85).aspx">PathGradientBrush::SetBlend</a>.



