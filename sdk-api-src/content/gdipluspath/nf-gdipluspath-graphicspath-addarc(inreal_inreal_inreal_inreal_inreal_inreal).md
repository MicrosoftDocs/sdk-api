---
UID: NF:gdipluspath.GraphicsPath.AddArc(INREAL,INREAL,INREAL,INREAL,INREAL,INREAL)
title: GraphicsPath::AddArc(IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL) (gdipluspath.h)
description: The GraphicsPath::AddArc method adds an elliptical arc to the current figure of this path.
helpviewer_keywords: ["AddArc","AddArc method [GDI+]","AddArc method [GDI+]","GraphicsPath class","GraphicsPath class [GDI+]","AddArc method","GraphicsPath.AddArc","GraphicsPath.AddArc(IN REAL","IN REAL","IN REAL","IN REAL","IN REAL","IN REAL)","GraphicsPath.AddArc(REAL","REAL","REAL","REAL","REAL","REAL)","GraphicsPath::AddArc","GraphicsPath::AddArc(IN REAL","IN REAL","IN REAL","IN REAL","IN REAL","IN REAL)","_gdiplus_CLASS_GraphicsPath_AddArc_REAL_x_REAL_y_REAL_width_REAL_height_REAL_startAngle_REAL_sweepAn","gdiplus._gdiplus_CLASS_GraphicsPath_AddArc_REAL_x_REAL_y_REAL_width_REAL_height_REAL_startAngle_REAL_sweepAn"]
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_AddArc_REAL_x_REAL_y_REAL_width_REAL_height_REAL_startAngle_REAL_sweepAn.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\graphicspathaddarcmethods\addarc_3realx_realy_realwidth_realheight_realst.htm
ms.date: 12/05/2018
ms.keywords: AddArc, AddArc method [GDI+], AddArc method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],AddArc method, GraphicsPath.AddArc, GraphicsPath.AddArc(IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL), GraphicsPath.AddArc(REAL,REAL,REAL,REAL,REAL,REAL), GraphicsPath::AddArc, GraphicsPath::AddArc(IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL), _gdiplus_CLASS_GraphicsPath_AddArc_REAL_x_REAL_y_REAL_width_REAL_height_REAL_startAngle_REAL_sweepAn, gdiplus._gdiplus_CLASS_GraphicsPath_AddArc_REAL_x_REAL_y_REAL_width_REAL_height_REAL_startAngle_REAL_sweepAn
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
 - GraphicsPath::AddArc
 - gdipluspath/GraphicsPath::AddArc
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
 - GraphicsPath.AddArc
---

# GraphicsPath::AddArc(IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL)


## -description

The <b>GraphicsPath::AddArc</b> method adds an elliptical arc to the current figure of this path.

## -parameters

### -param x [in]

Type: <b>REAL</b>

Real number that specifies the x-coordinate of the upper-left corner of the bounding rectangle for the ellipse that contains the arc.

### -param y [in]

Type: <b>REAL</b>

Real number that specifies the y-coordinate of the upper-left corner of the bounding rectangle for the ellipse that contains the arc.

### -param width [in]

Type: <b>REAL</b>

Real number that specifies the width of the bounding rectangle for the ellipse that contains the arc.

### -param height [in]

Type: <b>REAL</b>

Real number that specifies the height of the bounding rectangle for the ellipse that contains the arc.

### -param startAngle [in]

Type: <b>REAL</b>

Real number that specifies the clockwise angle, in degrees, between the horizontal axis of the ellipse and the starting point of the arc.

### -param sweepAngle [in]

Type: <b>REAL</b>

Real number that specifies the clockwise angle, in degrees, between the starting point (<i>startAngle</i>) and the ending point of the arc.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-addarc(inconstrect__inreal_inreal)">AddArc Methods</a>



<a href="/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>



<a href="/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inconstrectf__inreal_inreal)">DrawArc Methods</a>



<a href="/windows/desktop/gdiplus/-gdiplus-ellipses-and-arcs-about">Ellipses and Arcs</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>