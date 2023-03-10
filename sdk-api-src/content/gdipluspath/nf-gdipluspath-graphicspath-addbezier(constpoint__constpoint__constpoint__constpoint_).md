---
UID: NF:gdipluspath.GraphicsPath.AddBezier(constPoint&,constPoint&,constPoint&,constPoint&)
title: GraphicsPath::AddBezier(IN const Point &,IN const Point &,IN const Point &,IN const Point &) (gdipluspath.h)
description: The GraphicsPath::AddBezier method adds a B�zier spline to the current figure of this path. (overload 2/3)
helpviewer_keywords: ["AddBezier","AddBezier method [GDI+]","AddBezier method [GDI+]","GraphicsPath class","GraphicsPath class [GDI+]","AddBezier method","GraphicsPath.AddBezier","GraphicsPath.AddBezier(IN const Point &","IN const Point &","IN const Point &","IN const Point &)","GraphicsPath.AddBezier(const Point&","const Point&","const Point&","const Point&)","GraphicsPath::AddBezier","GraphicsPath::AddBezier(IN const Point &","IN const Point &","IN const Point &","IN const Point &)","_gdiplus_CLASS_GraphicsPath_AddBezier_Point_pt1_Point_pt2_Point_pt3_Point_pt4_","gdiplus._gdiplus_CLASS_GraphicsPath_AddBezier_Point_pt1_Point_pt2_Point_pt3_Point_pt4_"]
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_AddBezier_Point_pt1_Point_pt2_Point_pt3_Point_pt4_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\graphicspathaddbeziermethods\addbezier.htm
ms.date: 12/05/2018
ms.keywords: AddBezier, AddBezier method [GDI+], AddBezier method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],AddBezier method, GraphicsPath.AddBezier, GraphicsPath.AddBezier(IN const Point &,IN const Point &,IN const Point &,IN const Point &), GraphicsPath.AddBezier(const Point&,const Point&,const Point&,const Point&), GraphicsPath::AddBezier, GraphicsPath::AddBezier(IN const Point &,IN const Point &,IN const Point &,IN const Point &), _gdiplus_CLASS_GraphicsPath_AddBezier_Point_pt1_Point_pt2_Point_pt3_Point_pt4_, gdiplus._gdiplus_CLASS_GraphicsPath_AddBezier_Point_pt1_Point_pt2_Point_pt3_Point_pt4_
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
 - GraphicsPath::AddBezier
 - gdipluspath/GraphicsPath::AddBezier
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
 - GraphicsPath.AddBezier
---

# GraphicsPath::AddBezier(IN const Point &,IN const Point &,IN const Point &,IN const Point &)


## -description

The <b>GraphicsPath::AddBezier</b> method adds a Bézier spline to the current figure of this path.

## -parameters

### -param pt1 [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a></b>

Reference to a point at which to start the Bézier spline.

### -param pt2 [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a></b>

Reference to a point that is the first control point of the Bézier spline.

### -param pt3 [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a></b>

Reference to a point that is the second control point of the Bézier spline.

### -param pt4 [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a></b>

Reference to a point at which to end the Bézier spline.

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



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>
