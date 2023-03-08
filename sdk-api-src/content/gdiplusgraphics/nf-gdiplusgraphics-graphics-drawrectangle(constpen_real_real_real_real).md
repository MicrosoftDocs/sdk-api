---
UID: NF:gdiplusgraphics.Graphics.DrawRectangle(constPen,REAL,REAL,REAL,REAL)
title: Graphics::DrawRectangle(IN const Pen,IN REAL,IN REAL,IN REAL,IN REAL) (gdiplusgraphics.h)
description: The Graphics::DrawRectangle method draws a rectangle. (overload 1/4)
helpviewer_keywords: ["DrawRectangle","DrawRectangle method [GDI+]","DrawRectangle method [GDI+]","Graphics class","Graphics class [GDI+]","DrawRectangle method","Graphics.DrawRectangle","Graphics.DrawRectangle(IN const Pen","IN REAL","IN REAL","IN REAL","IN REAL)","Graphics.DrawRectangle(const Pen*","REAL","REAL","REAL","REAL)","Graphics::DrawRectangle","Graphics::DrawRectangle(IN const Pen","IN REAL","IN REAL","IN REAL","IN REAL)","_gdiplus_CLASS_Graphics_DrawRectangle_Pen_pen_REAL_x_REAL_y_REAL_width_REAL_height_","gdiplus._gdiplus_CLASS_Graphics_DrawRectangle_Pen_pen_REAL_x_REAL_y_REAL_width_REAL_height_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawRectangle_Pen_pen_REAL_x_REAL_y_REAL_width_REAL_height_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawrectanglemethods\drawrectangle_65penpen_realx_realy_realwidth_realheigh.htm
ms.date: 12/05/2018
ms.keywords: DrawRectangle, DrawRectangle method [GDI+], DrawRectangle method [GDI+],Graphics class, Graphics class [GDI+],DrawRectangle method, Graphics.DrawRectangle, Graphics.DrawRectangle(IN const Pen,IN REAL,IN REAL,IN REAL,IN REAL), Graphics.DrawRectangle(const Pen*,REAL,REAL,REAL,REAL), Graphics::DrawRectangle, Graphics::DrawRectangle(IN const Pen,IN REAL,IN REAL,IN REAL,IN REAL), _gdiplus_CLASS_Graphics_DrawRectangle_Pen_pen_REAL_x_REAL_y_REAL_width_REAL_height_, gdiplus._gdiplus_CLASS_Graphics_DrawRectangle_Pen_pen_REAL_x_REAL_y_REAL_width_REAL_height_
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
 - Graphics::DrawRectangle
 - gdiplusgraphics/Graphics::DrawRectangle
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
 - Graphics.DrawRectangle
---

# Graphics::DrawRectangle(IN const Pen,IN REAL,IN REAL,IN REAL,IN REAL)


## -description

The <b>Graphics::DrawRectangle</b> method draws a rectangle.

## -parameters

### -param pen [in]

Type: <b>const <a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> that is used to draw the rectangle.

### -param x [in]

Type: <b>REAL</b>

Real number that specifies the x-coordinate of the upper-left corner of the rectangle.

### -param y [in]

Type: <b>REAL</b>

Real number that specifies the y-coordinate of the upper-left corner of the rectangle.

### -param width [in]

Type: <b>REAL</b>

Real number that specifies the width of the rectangle.

### -param height [in]

Type: <b>REAL</b>

Real number that specifies the height of the rectangle.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangles(inconstpen_inconstrect_inint)">DrawRectangles Methods</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inconstrect_)">FillRectangle Methods</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-a-pen-to-draw-lines-and-rectangles-use">Using a Pen to Draw Lines and Rectangles</a>
