---
UID: NF:gdipluspath.PathGradientBrush.PathGradientBrush(IN const Point,IN INT,IN WrapMode)
title: PathGradientBrush::PathGradientBrush(IN const Point,IN INT,IN WrapMode)
author: windows-sdk-content
description: Creates a PathGradientBrush::PathGradientBrush object based on an array of points. Initializes the wrap mode of the path gradient brush.
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_PathGradientBrush_Point_points_INT_count_WrapMode_wrapMode_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushconstructors\pathgradientbrush_15pointpoints_intcount_wrapmodewrapmode.htm
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: PathGradientBrush, PathGradientBrush class [GDI+],PathGradientBrush constructor, PathGradientBrush constructor [GDI+], PathGradientBrush constructor [GDI+],PathGradientBrush class, PathGradientBrush.PathGradientBrush, PathGradientBrush.PathGradientBrush(IN const Point,IN INT,IN WrapMode), PathGradientBrush.PathGradientBrush(const Point*,INT,WrapMode), PathGradientBrush::PathGradientBrush, PathGradientBrush::PathGradientBrush(IN const Point,IN INT,IN WrapMode), _gdiplus_CLASS_PathGradientBrush_PathGradientBrush_Point_points_INT_count_WrapMode_wrapMode_, gdiplus._gdiplus_CLASS_PathGradientBrush_PathGradientBrush_Point_points_INT_count_WrapMode_wrapMode_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdipluspath.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - PathGradientBrush.PathGradientBrush
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# PathGradientBrush::PathGradientBrush(IN const Point,IN INT,IN WrapMode)


## -description


Creates a <b>PathGradientBrush::PathGradientBrush</b> object based on an array of points. Initializes the wrap mode of the path gradient brush.


## -parameters




### -param points [in]

Type: <b>const <a href="https://msdn.microsoft.com/8bf4d566-b061-4102-8307-218431e286f8">Point</a>*</b>

Pointer to an array of points that specifies the boundary path of the path gradient brush. 


### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the <i>points</i> array. 


### -param wrapMode [in]

Type: <b><a href="https://msdn.microsoft.com/24b035f9-c03e-4502-b603-d6a9e47d6df9">WrapMode</a></b>

Optional. Element of the <a href="https://msdn.microsoft.com/24b035f9-c03e-4502-b603-d6a9e47d6df9">WrapMode</a> enumeration that specifies how areas painted with the path gradient brush will be tiled. The default value is WrapModeClamp. 


## -see-also




<a href="https://msdn.microsoft.com/889558d5-9181-43ff-b862-e92966324208">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/f6a8085c-3d6a-494f-a1ee-5fa96efb1aae">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/7aa94b39-bd4c-4e66-b0dc-77f8953797b1">Filling a Shape with a Color Gradient</a>



<a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a>



<a href="https://msdn.microsoft.com/43901cd3-b059-4830-9063-e8287899e18a">LinearGradientBrush</a>



<a href="https://msdn.microsoft.com/cac0a3ce-982e-4de5-a160-cb8a755beddd">PathGradientBrush</a>



<a href="https://msdn.microsoft.com/8bf4d566-b061-4102-8307-218431e286f8">Point</a>
 

 

