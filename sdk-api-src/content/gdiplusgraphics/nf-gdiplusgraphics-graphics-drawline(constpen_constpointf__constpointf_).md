---
UID: NF:gdiplusgraphics.Graphics.DrawLine(constPen,constPointF&,constPointF&)
title: Graphics::DrawLine(IN const Pen,IN const PointF &,IN const PointF &) (gdiplusgraphics.h)
description: The Graphics::DrawLine method draws a line that connects two points. (overload 3/4)
helpviewer_keywords: ["DrawLine","DrawLine method [GDI+]","DrawLine method [GDI+]","Graphics class","Graphics class [GDI+]","DrawLine method","Graphics.DrawLine","Graphics.DrawLine(IN const Pen","IN const PointF &","IN const PointF &)","Graphics.DrawLine(const Pen*","const PointF&","const PointF&)","Graphics::DrawLine","Graphics::DrawLine(IN const Pen","IN const PointF &","IN const PointF &)","_gdiplus_CLASS_Graphics_DrawLine_Pen_pen_PointF_pt1_PointF_pt2_","gdiplus._gdiplus_CLASS_Graphics_DrawLine_Pen_pen_PointF_pt1_PointF_pt2_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawLine_Pen_pen_PointF_pt1_PointF_pt2_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawlinemethods\drawline_18penpen_pointfamppt1_pointfamppt2.htm
ms.date: 12/05/2018
ms.keywords: DrawLine, DrawLine method [GDI+], DrawLine method [GDI+],Graphics class, Graphics class [GDI+],DrawLine method, Graphics.DrawLine, Graphics.DrawLine(IN const Pen,IN const PointF &,IN const PointF &), Graphics.DrawLine(const Pen*,const PointF&,const PointF&), Graphics::DrawLine, Graphics::DrawLine(IN const Pen,IN const PointF &,IN const PointF &), _gdiplus_CLASS_Graphics_DrawLine_Pen_pen_PointF_pt1_PointF_pt2_, gdiplus._gdiplus_CLASS_Graphics_DrawLine_Pen_pen_PointF_pt1_PointF_pt2_
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
 - Graphics::DrawLine
 - gdiplusgraphics/Graphics::DrawLine
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
 - Graphics.DrawLine
---

# Graphics::DrawLine(IN const Pen,IN const PointF &,IN const PointF &)


## -description

The <b>Graphics::DrawLine</b> method draws a line that connects two points.

## -parameters

### -param pen [in]

Type: <b>const <a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>*</b>

Pointer to a pen that is used to draw the line.

### -param pt1 [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a></b>

Reference to a <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a> object that specifies the start of the line.

### -param pt2 [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a></b>

Reference to a <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a> object that specifies the end of the line.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawlines(inconstpen_inconstpoint_inint)">DrawLines Methods</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-a-pen-to-draw-lines-and-rectangles-use">Using a Pen to Draw Lines and Rectangles</a>
