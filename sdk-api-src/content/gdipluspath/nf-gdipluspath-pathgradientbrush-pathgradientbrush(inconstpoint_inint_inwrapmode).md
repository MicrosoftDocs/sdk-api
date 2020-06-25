---
UID: NF:gdipluspath.PathGradientBrush.PathGradientBrush(IN const Point,IN INT,IN WrapMode)
title: PathGradientBrush::PathGradientBrush(IN const Point,IN INT,IN WrapMode) (gdipluspath.h)
description: Creates a PathGradientBrush::PathGradientBrush object based on an array of points. Initializes the wrap mode of the path gradient brush.
helpviewer_keywords: ["PathGradientBrush","PathGradientBrush class [GDI+]","PathGradientBrush constructor","PathGradientBrush constructor [GDI+]","PathGradientBrush constructor [GDI+]","PathGradientBrush class","PathGradientBrush.PathGradientBrush","PathGradientBrush.PathGradientBrush(IN const Point","IN INT","IN WrapMode)","PathGradientBrush.PathGradientBrush(const Point*","INT","WrapMode)","PathGradientBrush::PathGradientBrush","PathGradientBrush::PathGradientBrush(IN const Point","IN INT","IN WrapMode)","_gdiplus_CLASS_PathGradientBrush_PathGradientBrush_Point_points_INT_count_WrapMode_wrapMode_","gdiplus._gdiplus_CLASS_PathGradientBrush_PathGradientBrush_Point_points_INT_count_WrapMode_wrapMode_"]
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_PathGradientBrush_Point_points_INT_count_WrapMode_wrapMode_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushconstructors\pathgradientbrush_15pointpoints_intcount_wrapmodewrapmode.htm
ms.date: 12/05/2018
ms.keywords: PathGradientBrush, PathGradientBrush class [GDI+],PathGradientBrush constructor, PathGradientBrush constructor [GDI+], PathGradientBrush constructor [GDI+],PathGradientBrush class, PathGradientBrush.PathGradientBrush, PathGradientBrush.PathGradientBrush(IN const Point,IN INT,IN WrapMode), PathGradientBrush.PathGradientBrush(const Point*,INT,WrapMode), PathGradientBrush::PathGradientBrush, PathGradientBrush::PathGradientBrush(IN const Point,IN INT,IN WrapMode), _gdiplus_CLASS_PathGradientBrush_PathGradientBrush_Point_points_INT_count_WrapMode_wrapMode_, gdiplus._gdiplus_CLASS_PathGradientBrush_PathGradientBrush_Point_points_INT_count_WrapMode_wrapMode_
f1_keywords:
- gdipluspath/PathGradientBrush.PathGradientBrush
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# PathGradientBrush::PathGradientBrush(IN const Point,IN INT,IN WrapMode)


## -description


Creates a <b>PathGradientBrush::PathGradientBrush</b> object based on an array of points. Initializes the wrap mode of the path gradient brush.


## -parameters




### -param points [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>*</b>

Pointer to an array of points that specifies the boundary path of the path gradient brush. 


### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the <i>points</i> array. 


### -param wrapMode [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-wrapmode">WrapMode</a></b>

Optional. Element of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-wrapmode">WrapMode</a> enumeration that specifies how areas painted with the path gradient brush will be tiled. The default value is WrapModeClamp. 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-filling-a-shape-with-a-color-gradient-use">Filling a Shape with a Color Gradient</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush">LinearGradientBrush</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>
 

 

