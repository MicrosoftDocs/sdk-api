---
UID: NF:gdipluspath.GraphicsPath.AddBeziers(constPoint,INT)
title: GraphicsPath::AddBeziers(IN const Point,IN INT) (gdipluspath.h)
description: The GraphicsPath::AddBeziers method adds a sequence of connected Bézier splines to the current figure of this path.
helpviewer_keywords: ["AddBeziers","AddBeziers method [GDI+]","AddBeziers method [GDI+]","GraphicsPath class","GraphicsPath class [GDI+]","AddBeziers method","GraphicsPath.AddBeziers","GraphicsPath.AddBeziers(IN const Point","IN INT)","GraphicsPath.AddBeziers(const PointF*","INT)","GraphicsPath::AddBeziers","GraphicsPath::AddBeziers(IN const Point","IN INT)","_gdiplus_CLASS_GraphicsPath_AddBeziers_PointF_points_INT_count_","gdiplus._gdiplus_CLASS_GraphicsPath_AddBeziers_PointF_points_INT_count_"]
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_AddBeziers_PointF_points_INT_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\graphicspathaddbeziersmethods\addbeziers_6pointfpoints_intcount.htm
ms.date: 12/05/2018
ms.keywords: AddBeziers, AddBeziers method [GDI+], AddBeziers method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],AddBeziers method, GraphicsPath.AddBeziers, GraphicsPath.AddBeziers(IN const Point,IN INT), GraphicsPath.AddBeziers(const PointF*,INT), GraphicsPath::AddBeziers, GraphicsPath::AddBeziers(IN const Point,IN INT), _gdiplus_CLASS_GraphicsPath_AddBeziers_PointF_points_INT_count_, gdiplus._gdiplus_CLASS_GraphicsPath_AddBeziers_PointF_points_INT_count_
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
 - GraphicsPath::AddBeziers
 - gdipluspath/GraphicsPath::AddBeziers
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
 - GraphicsPath.AddBeziers
---

# GraphicsPath::AddBeziers(IN const Point,IN INT)


## -description

The <b>GraphicsPath::AddBeziers</b> method adds a sequence of connected Bézier splines to the current figure of this path.

## -parameters

### -param points [in]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a>*</b>

Pointer to an array of starting points, ending points, and control points for the connected splines. The first spline is constructed from the first point through the fourth point in the array and uses the second and third points as control points. Each subsequent spline in the sequence needs exactly three more points: the ending point of the previous spline is used as the starting point, the next two points in the sequence are control points, and the third point is the ending point.

### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the <i>points</i> array.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-addbezier(inconstpoint__inconstpoint__inconstpoint__inconstpoint_)">AddBezier Methods</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-addbeziers(inconstpoint_inint)">AddBeziers Methods</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpointf_inint_inint_inint_inreal)">AddCurve Methods</a>



<a href="/windows/desktop/gdiplus/-gdiplus-bezier-splines-about">Bézier Splines</a>



<a href="/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>



<a href="/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="/windows/desktop/gdiplus/-gdiplus-drawing-bezier-splines-use">Drawing Bézier Splines</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a>