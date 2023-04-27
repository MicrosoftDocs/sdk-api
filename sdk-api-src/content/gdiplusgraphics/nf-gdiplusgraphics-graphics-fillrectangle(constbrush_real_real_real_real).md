---
UID: NF:gdiplusgraphics.Graphics.FillRectangle(constBrush,REAL,REAL,REAL,REAL)
title: Graphics::FillRectangle(IN const Brush,IN REAL,IN REAL,IN REAL,IN REAL) (gdiplusgraphics.h)
description: The Graphics::FillRectangle method uses a brush to fill the interior of a rectangle. (overload 4/4)
helpviewer_keywords: ["FillRectangle","FillRectangle method [GDI+]","FillRectangle method [GDI+]","Graphics class","Graphics class [GDI+]","FillRectangle method","Graphics.FillRectangle","Graphics.FillRectangle(IN const Brush","IN REAL","IN REAL","IN REAL","IN REAL)","Graphics.FillRectangle(const Brush*","REAL","REAL","REAL","REAL)","Graphics::FillRectangle","Graphics::FillRectangle(IN const Brush","IN REAL","IN REAL","IN REAL","IN REAL)","_gdiplus_CLASS_Graphics_FillRectangle_Brush_brush_REAL_x_REAL_y_REAL_width_REAL_height_","gdiplus._gdiplus_CLASS_Graphics_FillRectangle_Brush_brush_REAL_x_REAL_y_REAL_width_REAL_height_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_FillRectangle_Brush_brush_REAL_x_REAL_y_REAL_width_REAL_height_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsfillrectanglemethods\fillrectangle_55brushbrush_realx_realy_realwidth_realh.htm
ms.date: 12/05/2018
ms.keywords: FillRectangle, FillRectangle method [GDI+], FillRectangle method [GDI+],Graphics class, Graphics class [GDI+],FillRectangle method, Graphics.FillRectangle, Graphics.FillRectangle(IN const Brush,IN REAL,IN REAL,IN REAL,IN REAL), Graphics.FillRectangle(const Brush*,REAL,REAL,REAL,REAL), Graphics::FillRectangle, Graphics::FillRectangle(IN const Brush,IN REAL,IN REAL,IN REAL,IN REAL), _gdiplus_CLASS_Graphics_FillRectangle_Brush_brush_REAL_x_REAL_y_REAL_width_REAL_height_, gdiplus._gdiplus_CLASS_Graphics_FillRectangle_Brush_brush_REAL_x_REAL_y_REAL_width_REAL_height_
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
 - Graphics::FillRectangle
 - gdiplusgraphics/Graphics::FillRectangle
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
 - Graphics.FillRectangle
---

# Graphics::FillRectangle(IN const Brush,IN REAL,IN REAL,IN REAL,IN REAL)


## -description

The <b>Graphics::FillRectangle</b> method uses a brush to fill the interior of a rectangle.

## -parameters

### -param brush [in]

Type: <b>const <a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush">Brush</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush">Brush</a> that is used to paint the interior of the rectangle.

### -param x [in]

Type: <b>REAL</b>

Real number that specifies the x-coordinate of the upper-left corner of the rectangle to be filled.

### -param y [in]

Type: <b>REAL</b>

Real number that specifies the y-coordinate of the upper-left corner of the rectangle to be filled.

### -param width [in]

Type: <b>REAL</b>

Real number that specifies the width of the rectangle to be filled.

### -param height [in]

Type: <b>REAL</b>

Real number that specifies the height of the rectangle to be filled.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>



<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>
