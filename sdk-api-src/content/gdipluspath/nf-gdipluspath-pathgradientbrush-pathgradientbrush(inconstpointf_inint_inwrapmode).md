---
UID: NF:gdipluspath.PathGradientBrush.PathGradientBrush(IN const PointF,IN INT,IN WrapMode)
title: PathGradientBrush::PathGradientBrush(IN const PointF,IN INT,IN WrapMode)
author: windows-sdk-content
description: Creates a PathGradientBrush object based on an array of points. Initializes the wrap mode of the path gradient brush.
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_PathGradientBrush_PointF_points_INT_count_WrapMode_wrapMode_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushconstructors\pathgradientbrush_26pointfpoints_intcount_wrapmodewrapmode.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PathGradientBrush, PathGradientBrush class [GDI+],PathGradientBrush constructor, PathGradientBrush constructor [GDI+], PathGradientBrush constructor [GDI+],PathGradientBrush class, PathGradientBrush.PathGradientBrush, PathGradientBrush.PathGradientBrush(IN const PointF,IN INT,IN WrapMode), PathGradientBrush.PathGradientBrush(const PointF*,INT,WrapMode), PathGradientBrush::PathGradientBrush, PathGradientBrush::PathGradientBrush(IN const PointF,IN INT,IN WrapMode), _gdiplus_CLASS_PathGradientBrush_PathGradientBrush_PointF_points_INT_count_WrapMode_wrapMode_, gdiplus._gdiplus_CLASS_PathGradientBrush_PathGradientBrush_PointF_points_INT_count_WrapMode_wrapMode_
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

# PathGradientBrush::PathGradientBrush(IN const PointF,IN INT,IN WrapMode)


## -description


Creates a <a href="https://msdn.microsoft.com/en-us/library/ms534483(v=VS.85).aspx">PathGradientBrush</a> object based on an array of points. Initializes the wrap mode of the path gradient brush.


## -parameters




### -param points [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534488(v=VS.85).aspx">PointF</a>*</b>

Pointer to an array of points that specifies the boundary path of the path gradient brush. 


### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the <i>points</i> array. 


### -param wrapMode [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534407(v=VS.85).aspx">WrapMode</a></b>

Optional. Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534407(v=VS.85).aspx">WrapMode</a> enumeration that specifies how areas painted with the path gradient brush will be tiled. The default value is WrapModeClamp. 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms536356(v=VS.85).aspx">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533917(v=VS.85).aspx">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533856(v=VS.85).aspx">Filling a Shape with a Color Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534473(v=VS.85).aspx">LinearGradientBrush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534483(v=VS.85).aspx">PathGradientBrush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534488(v=VS.85).aspx">PointF</a>
 

 

