---
UID: NF:gdiplusgraphics.Graphics.DrawEllipse(constPen,constRect&)
title: Graphics::DrawEllipse(IN const Pen,IN const Rect &) (gdiplusgraphics.h)
description: The Graphics::DrawEllipse method draws an ellipse. (overload 2/4)
helpviewer_keywords: ["DrawEllipse","DrawEllipse method [GDI+]","DrawEllipse method [GDI+]","Graphics class","Graphics class [GDI+]","DrawEllipse method","Graphics.DrawEllipse","Graphics.DrawEllipse(IN const Pen","IN const Rect &)","Graphics.DrawEllipse(const Pen*","const Rect&)","Graphics::DrawEllipse","Graphics::DrawEllipse(IN const Pen","IN const Rect &)","_gdiplus_CLASS_Graphics_DrawEllipse_Pen_pen_Rect_rect_","gdiplus._gdiplus_CLASS_Graphics_DrawEllipse_Pen_pen_Rect_rect_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawEllipse_Pen_pen_Rect_rect_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawellipsemethods\drawellipse.htm
ms.date: 12/05/2018
ms.keywords: DrawEllipse, DrawEllipse method [GDI+], DrawEllipse method [GDI+],Graphics class, Graphics class [GDI+],DrawEllipse method, Graphics.DrawEllipse, Graphics.DrawEllipse(IN const Pen,IN const Rect &), Graphics.DrawEllipse(const Pen*,const Rect&), Graphics::DrawEllipse, Graphics::DrawEllipse(IN const Pen,IN const Rect &), _gdiplus_CLASS_Graphics_DrawEllipse_Pen_pen_Rect_rect_, gdiplus._gdiplus_CLASS_Graphics_DrawEllipse_Pen_pen_Rect_rect_
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
 - Graphics::DrawEllipse
 - gdiplusgraphics/Graphics::DrawEllipse
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
 - Graphics.DrawEllipse
---

# Graphics::DrawEllipse(IN const Pen,IN const Rect &)


## -description

The <b>Graphics::DrawEllipse</b> method draws an ellipse.

## -parameters

### -param pen [in]

Type: <b>const <a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>*</b>

Pointer to a pen that is used to draw the ellipse.

### -param rect [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a></b>

Reference to a rectangle that bounds the ellipse.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-ellipses-and-arcs-about">Ellipses and Arcs</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inconstrect_)">FillEllipse Methods</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>
