---
UID: NF:gdipluspath.GraphicsPath.AddBezier(INT,INT,INT,INT,INT,INT,INT,INT)
title: GraphicsPath::AddBezier(IN INT,IN INT,IN INT,IN INT,IN INT,IN INT,IN INT,IN INT) (gdipluspath.h)
description: The GraphicsPath::AddBezier method adds a Bézier spline to the current figure of this path. (overload 3/3)
helpviewer_keywords: ["AddBezier","AddBezier method [GDI+]","AddBezier method [GDI+]","GraphicsPath class","GraphicsPath class [GDI+]","AddBezier method","GraphicsPath.AddBezier","GraphicsPath.AddBezier(IN INT","IN INT","IN INT","IN INT","IN INT","IN INT","IN INT","IN INT)","GraphicsPath.AddBezier(INT","INT","INT","INT","INT","INT","INT","INT)","GraphicsPath::AddBezier","GraphicsPath::AddBezier(IN INT","IN INT","IN INT","IN INT","IN INT","IN INT","IN INT","IN INT)","_gdiplus_CLASS_GraphicsPath_AddBezier_INT_x1_INT_y1_INT_x2_INT_y2_INT_x3_INT_y3_INT_x4_INT_y4_","gdiplus._gdiplus_CLASS_GraphicsPath_AddBezier_INT_x1_INT_y1_INT_x2_INT_y2_INT_x3_INT_y3_INT_x4_INT_y4_"]
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_AddBezier_INT_x1_INT_y1_INT_x2_INT_y2_INT_x3_INT_y3_INT_x4_INT_y4_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\graphicspathaddbeziermethods\addbezier_86intx1_inty1_intx2_inty2_intx3_inty3_in.htm
ms.date: 12/05/2018
ms.keywords: AddBezier, AddBezier method [GDI+], AddBezier method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],AddBezier method, GraphicsPath.AddBezier, GraphicsPath.AddBezier(IN INT,IN INT,IN INT,IN INT,IN INT,IN INT,IN INT,IN INT), GraphicsPath.AddBezier(INT,INT,INT,INT,INT,INT,INT,INT), GraphicsPath::AddBezier, GraphicsPath::AddBezier(IN INT,IN INT,IN INT,IN INT,IN INT,IN INT,IN INT,IN INT), _gdiplus_CLASS_GraphicsPath_AddBezier_INT_x1_INT_y1_INT_x2_INT_y2_INT_x3_INT_y3_INT_x4_INT_y4_, gdiplus._gdiplus_CLASS_GraphicsPath_AddBezier_INT_x1_INT_y1_INT_x2_INT_y2_INT_x3_INT_y3_INT_x4_INT_y4_
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

# GraphicsPath::AddBezier(IN INT,IN INT,IN INT,IN INT,IN INT,IN INT,IN INT,IN INT)


## -description

The <b>GraphicsPath::AddBezier</b> method adds a Bézier spline to the current figure of this path.

## -parameters

### -param x1 [in]

Type: <b>INT</b>

Integer that specifies the x-coordinate of the starting point of the Bézier spline.

### -param y1 [in]

Type: <b>INT</b>

Integer that specifies the y-coordinate of the starting point of the Bézier spline.

### -param x2 [in]

Type: <b>INT</b>

Integer that specifies the x-coordinate of the first control point of the Bézier spline.

### -param y2 [in]

Type: <b>INT</b>

Integer that specifies the y-coordinate of the first control point of the Bézier spline.

### -param x3 [in]

Type: <b>INT</b>

Integer that specifies the x-coordinate of the second control point of the Bézier spline.

### -param y3 [in]

Type: <b>INT</b>

Integer that specifies the y-coordinate of the second control point of the Bézier spline.

### -param x4 [in]

Type: <b>INT</b>

Integer that specifies the x-coordinate of the ending point of the Bézier spline.

### -param y4 [in]

Type: <b>INT</b>

Integer that specifies the y-coordinate of the ending point of the Bézier spline.

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
