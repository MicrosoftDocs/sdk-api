---
UID: NF:gdiplusgraphics.Graphics.DrawRectangles(constPen,constRect,INT)
title: Graphics::DrawRectangles(IN const Pen,IN const Rect,IN INT) (gdiplusgraphics.h)
description: The Graphics::DrawRectangles method draws a sequence of rectangles. (overload 1/2)
helpviewer_keywords: ["DrawRectangles","DrawRectangles method [GDI+]","DrawRectangles method [GDI+]","Graphics class","Graphics class [GDI+]","DrawRectangles method","Graphics.DrawRectangles","Graphics.DrawRectangles(IN const Pen","IN const Rect","IN INT)","Graphics.DrawRectangles(const Pen*","const Rect*","INT)","Graphics::DrawRectangles","Graphics::DrawRectangles(IN const Pen","IN const Rect","IN INT)","_gdiplus_CLASS_Graphics_DrawRectangles_Pen_pen_Rect_rects_INT_count_","gdiplus._gdiplus_CLASS_Graphics_DrawRectangles_Pen_pen_Rect_rects_INT_count_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawRectangles_Pen_pen_Rect_rects_INT_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawrectanglesmethods\drawrectangles.htm
ms.date: 12/05/2018
ms.keywords: DrawRectangles, DrawRectangles method [GDI+], DrawRectangles method [GDI+],Graphics class, Graphics class [GDI+],DrawRectangles method, Graphics.DrawRectangles, Graphics.DrawRectangles(IN const Pen,IN const Rect,IN INT), Graphics.DrawRectangles(const Pen*,const Rect*,INT), Graphics::DrawRectangles, Graphics::DrawRectangles(IN const Pen,IN const Rect,IN INT), _gdiplus_CLASS_Graphics_DrawRectangles_Pen_pen_Rect_rects_INT_count_, gdiplus._gdiplus_CLASS_Graphics_DrawRectangles_Pen_pen_Rect_rects_INT_count_
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
 - Graphics::DrawRectangles
 - gdiplusgraphics/Graphics::DrawRectangles
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
 - Graphics.DrawRectangles
---

# Graphics::DrawRectangles(IN const Pen,IN const Rect,IN INT)


## -description

The <b>Graphics::DrawRectangles</b> method draws a sequence of rectangles.

## -parameters

### -param pen [in]

Type: <b>const <a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> that is used to draw the rectangles.

### -param rects [in]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>*</b>

Pointer to an array of <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a> objects that specify the coordinates of the rectangles to be drawn.

### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the <i>rects</i> array.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangles(inconstpen_inconstrect_inint)">DrawRectangles Methods</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inconstrect_)">FillRectangle Methods</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-a-pen-to-draw-lines-and-rectangles-use">Using a Pen to Draw Lines and Rectangles</a>
