---
UID: NF:gdipluspath.PathGradientBrush.SetCenterPoint(constPoint&)
title: PathGradientBrush::SetCenterPoint(IN const Point &) (gdipluspath.h)
description: The PathGradientBrush::SetCenterPoint method sets the center point of this path gradient brush. By default, the center point is at the centroid of the brush's boundary path, but you can set the center point to any location inside or outside the path.
helpviewer_keywords: ["PathGradientBrush class [GDI+]","SetCenterPoint method","PathGradientBrush.SetCenterPoint","PathGradientBrush.SetCenterPoint(IN const Point &)","PathGradientBrush.SetCenterPoint(const Point&)","PathGradientBrush::SetCenterPoint","PathGradientBrush::SetCenterPoint(IN const Point &)","SetCenterPoint","SetCenterPoint method [GDI+]","SetCenterPoint method [GDI+]","PathGradientBrush class","_gdiplus_CLASS_PathGradientBrush_SetCenterPoint_Point_point_","gdiplus._gdiplus_CLASS_PathGradientBrush_SetCenterPoint_Point_point_"]
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_SetCenterPoint_Point_point_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushmethods\pathgradientbrushsetcenterpointmethods\setcenterpoint.htm
ms.date: 12/05/2018
ms.keywords: PathGradientBrush class [GDI+],SetCenterPoint method, PathGradientBrush.SetCenterPoint, PathGradientBrush.SetCenterPoint(IN const Point &), PathGradientBrush.SetCenterPoint(const Point&), PathGradientBrush::SetCenterPoint, PathGradientBrush::SetCenterPoint(IN const Point &), SetCenterPoint, SetCenterPoint method [GDI+], SetCenterPoint method [GDI+],PathGradientBrush class, _gdiplus_CLASS_PathGradientBrush_SetCenterPoint_Point_point_, gdiplus._gdiplus_CLASS_PathGradientBrush_SetCenterPoint_Point_point_
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - PathGradientBrush::SetCenterPoint
 - gdipluspath/PathGradientBrush::SetCenterPoint
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - PathGradientBrush.SetCenterPoint
---

# PathGradientBrush::SetCenterPoint(IN const Point &)


## -description

The <b>PathGradientBrush::SetCenterPoint</b> method sets the center point of this path gradient brush. By default, the center point is at the centroid of the brush's boundary path, but you can set the center point to any location inside or outside the path.

## -parameters

### -param point [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a></b>

Reference to a 
					<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a> object that specifies the center point.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="/windows/desktop/gdiplus/-gdiplus-filling-a-shape-with-a-color-gradient-use">Filling a Shape with a Color Gradient</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-getcentercolor">PathGradientBrush::GetCenterColor</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-getcenterpoint(outpoint)">PathGradientBrush::GetCenterPoint Methods</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcentercolor">PathGradientBrush::SetCenterColor</a>