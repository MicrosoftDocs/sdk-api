---
UID: NF:gdiplusgraphics.Graphics.DrawArc(INconstPen,INconstRect&,INREAL,INREAL)
title: Graphics::DrawArc(IN const Pen,IN const Rect &,IN REAL,IN REAL) (gdiplusgraphics.h)
description: The Graphics::DrawArc method draws an arc. The arc is part of an ellipse.
helpviewer_keywords: ["DrawArc","DrawArc method [GDI+]","DrawArc method [GDI+]","Graphics class","Graphics class [GDI+]","DrawArc method","Graphics.DrawArc","Graphics.DrawArc(IN const Pen","IN const Rect &","IN REAL","IN REAL)","Graphics.DrawArc(const Pen*","const Rect&","REAL","REAL)","Graphics::DrawArc","Graphics::DrawArc(IN const Pen","IN const Rect &","IN REAL","IN REAL)","_gdiplus_CLASS_Graphics_DrawArc_Pen_pen_Rect_rect_REAL_startAngle_REAL_sweepAngle_","gdiplus._gdiplus_CLASS_Graphics_DrawArc_Pen_pen_Rect_rect_REAL_startAngle_REAL_sweepAngle_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawArc_Pen_pen_Rect_rect_REAL_startAngle_REAL_sweepAngle_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawarcmethods\drawarc.htm
ms.date: 12/05/2018
ms.keywords: DrawArc, DrawArc method [GDI+], DrawArc method [GDI+],Graphics class, Graphics class [GDI+],DrawArc method, Graphics.DrawArc, Graphics.DrawArc(IN const Pen,IN const Rect &,IN REAL,IN REAL), Graphics.DrawArc(const Pen*,const Rect&,REAL,REAL), Graphics::DrawArc, Graphics::DrawArc(IN const Pen,IN const Rect &,IN REAL,IN REAL), _gdiplus_CLASS_Graphics_DrawArc_Pen_pen_Rect_rect_REAL_startAngle_REAL_sweepAngle_, gdiplus._gdiplus_CLASS_Graphics_DrawArc_Pen_pen_Rect_rect_REAL_startAngle_REAL_sweepAngle_
req.header: gdiplusgraphics.h
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
 - Graphics::DrawArc
 - gdiplusgraphics/Graphics::DrawArc
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
 - Graphics.DrawArc
---

# Graphics::DrawArc(IN const Pen,IN const Rect &,IN REAL,IN REAL)


## -description

The <b>Graphics::DrawArc</b> method draws an arc. The arc is part of an ellipse.

## -parameters

### -param pen [in]

Type: <b>const <a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>*</b>

Pointer to a pen that is used to draw the arc.

### -param rect [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a></b>

Reference to the rectangle that bounds the ellipse that contains the arc.

### -param startAngle [in]

Type: <b>REAL</b>

Real number that specifies the angle between the x-axis and the starting point of the arc.

### -param sweepAngle [in]

Type: <b>REAL</b>

Real number that specifies the angle between the starting and ending points of the arc.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the 
						<b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-creating-figures-from-lines-curves-and-shapes-use">Creating Figures from Lines, Curves, and Shapes</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inconstrectf__inreal_inreal)">DrawArc Methods</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)">DrawEllipse Methods</a>



<a href="/windows/desktop/gdiplus/-gdiplus-ellipses-and-arcs-about">Ellipses and Arcs</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>