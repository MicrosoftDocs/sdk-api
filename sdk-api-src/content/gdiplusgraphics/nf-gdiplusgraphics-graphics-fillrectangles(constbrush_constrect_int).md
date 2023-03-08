---
UID: NF:gdiplusgraphics.Graphics.FillRectangles(constBrush,constRect,INT)
title: Graphics::FillRectangles(IN const Brush,IN const Rect,IN INT) (gdiplusgraphics.h)
description: The Graphics::FillRectangles method uses a brush to fill the interior of a sequence of rectangles. (overload 2/2)
helpviewer_keywords: ["FillRectangles","FillRectangles method [GDI+]","FillRectangles method [GDI+]","Graphics class","Graphics class [GDI+]","FillRectangles method","Graphics.FillRectangles","Graphics.FillRectangles(IN const Brush","IN const Rect","IN INT)","Graphics.FillRectangles(const Brush*","const Rect*","INT)","Graphics::FillRectangles","Graphics::FillRectangles(IN const Brush","IN const Rect","IN INT)","_gdiplus_CLASS_Graphics_FillRectangles_Brush_brush_Rect_rects_INT_count_","gdiplus._gdiplus_CLASS_Graphics_FillRectangles_Brush_brush_Rect_rects_INT_count_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_FillRectangles_Brush_brush_Rect_rects_INT_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsfillrectanglesmethods\fillrectangles.htm
ms.date: 12/05/2018
ms.keywords: FillRectangles, FillRectangles method [GDI+], FillRectangles method [GDI+],Graphics class, Graphics class [GDI+],FillRectangles method, Graphics.FillRectangles, Graphics.FillRectangles(IN const Brush,IN const Rect,IN INT), Graphics.FillRectangles(const Brush*,const Rect*,INT), Graphics::FillRectangles, Graphics::FillRectangles(IN const Brush,IN const Rect,IN INT), _gdiplus_CLASS_Graphics_FillRectangles_Brush_brush_Rect_rects_INT_count_, gdiplus._gdiplus_CLASS_Graphics_FillRectangles_Brush_brush_Rect_rects_INT_count_
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
 - Graphics::FillRectangles
 - gdiplusgraphics/Graphics::FillRectangles
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
 - Graphics.FillRectangles
---

# Graphics::FillRectangles(IN const Brush,IN const Rect,IN INT)


## -description

The <b>Graphics::FillRectangles</b> method uses a brush to fill the interior of a sequence of rectangles.

## -parameters

### -param brush [in]

Type: <b>const <a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush">Brush</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush">Brush</a> that is used to fill the interior of each rectangle.

### -param rects [in]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>*</b>

Pointer to an array of rectangles to be filled.

### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of rectangles in the <i>rects</i> array.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>



<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>
