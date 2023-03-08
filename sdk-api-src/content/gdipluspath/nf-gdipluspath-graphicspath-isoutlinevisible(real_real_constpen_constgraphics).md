---
UID: NF:gdipluspath.GraphicsPath.IsOutlineVisible(REAL,REAL,constPen,constGraphics)
title: GraphicsPath::IsOutlineVisible(IN REAL,IN REAL,IN const Pen,IN const Graphics) (gdipluspath.h)
description: The GraphicsPath::IsOutlineVisible method determines whether a specified point touches the outline of this path when the path is drawn by a specified Graphics object and a specified pen. (overload 2/2)
helpviewer_keywords: ["GraphicsPath class [GDI+]","IsOutlineVisible method","GraphicsPath.IsOutlineVisible","GraphicsPath.IsOutlineVisible(IN REAL","IN REAL","IN const Pen","IN const Graphics)","GraphicsPath.IsOutlineVisible(REAL","REAL","const Pen*","const Graphics*)","GraphicsPath::IsOutlineVisible","GraphicsPath::IsOutlineVisible(IN REAL","IN REAL","IN const Pen","IN const Graphics)","IsOutlineVisible","IsOutlineVisible method [GDI+]","IsOutlineVisible method [GDI+]","GraphicsPath class","_gdiplus_CLASS_GraphicsPath_IsOutlineVisible_REAL_x_REAL_y_Pen_pen_Graphics_g_","gdiplus._gdiplus_CLASS_GraphicsPath_IsOutlineVisible_REAL_x_REAL_y_Pen_pen_Graphics_g_"]
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_IsOutlineVisible_REAL_x_REAL_y_Pen_pen_Graphics_g_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\graphicspathisoutlinevisiblemethods\isoutlinevisible_100realx_realy_penpen_graphicsg.htm
ms.date: 12/05/2018
ms.keywords: GraphicsPath class [GDI+],IsOutlineVisible method, GraphicsPath.IsOutlineVisible, GraphicsPath.IsOutlineVisible(IN REAL,IN REAL,IN const Pen,IN const Graphics), GraphicsPath.IsOutlineVisible(REAL,REAL,const Pen*,const Graphics*), GraphicsPath::IsOutlineVisible, GraphicsPath::IsOutlineVisible(IN REAL,IN REAL,IN const Pen,IN const Graphics), IsOutlineVisible, IsOutlineVisible method [GDI+], IsOutlineVisible method [GDI+],GraphicsPath class, _gdiplus_CLASS_GraphicsPath_IsOutlineVisible_REAL_x_REAL_y_Pen_pen_Graphics_g_, gdiplus._gdiplus_CLASS_GraphicsPath_IsOutlineVisible_REAL_x_REAL_y_Pen_pen_Graphics_g_
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
 - GraphicsPath::IsOutlineVisible
 - gdipluspath/GraphicsPath::IsOutlineVisible
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
 - GraphicsPath.IsOutlineVisible
---

# GraphicsPath::IsOutlineVisible(IN REAL,IN REAL,IN const Pen,IN const Graphics)


## -description

The <b>GraphicsPath::IsOutlineVisible</b> method determines whether a specified point touches the outline of this path when the path is drawn by a specified <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object and a specified pen.

## -parameters

### -param x [in]

Type: <b>REAL</b>

Real number that specifies the x-coordinate of the point to be tested.

### -param y [in]

Type: <b>REAL</b>

Real number that specifies the x-coordinate of the point to be tested.

### -param pen [in]

Type: <b>const <a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object. This method determines whether the test point touches the path outline that would be drawn by this pen. More points will touch an outline drawn by a wide pen than will touch an outline drawn by a narrow pen.

### -param g [in]

Type: <b>const <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>*</b>

Optional. Pointer to a <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object that specifies a world-to-device transformation. If the value of this parameter is <b>NULL</b>, the test is done in world coordinates; otherwise, the test is done in device coordinates. The default value is <b>NULL</b>.

## -returns

Type: <b>BOOL</b>

If the test point touches the outline of this path, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>



<a href="/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-isoutlinevisible(inconstpoint__inconstpen_inconstgraphics)">IsOutlineVisible Methods</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-isvisible(inconstpoint__inconstgraphics)">IsVisible Methods</a>



<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>



<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>



<a href="/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a>



<a href="/windows/desktop/gdiplus/-gdiplus-setting-pen-width-and-alignment-use">Setting Pen Width and Alignment</a>
