---
UID: NF:gdiplusgraphics.Graphics.DrawRectangle(IN const Pen,IN const Rect &)
title: Graphics::DrawRectangle(IN const Pen,IN const Rect &) (gdiplusgraphics.h)

description: The Graphics::DrawRectangle method draws a rectangle.
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawRectangle_Pen_pen_Rect_rect_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawrectanglemethods\drawrectangle.htm

ms.date: 12/05/2018
ms.keywords: DrawRectangle, DrawRectangle method [GDI+], DrawRectangle method [GDI+],Graphics class, Graphics class [GDI+],DrawRectangle method, Graphics.DrawRectangle, Graphics.DrawRectangle(IN const Pen,IN const Rect &), Graphics.DrawRectangle(const Pen*,const Rect&), Graphics::DrawRectangle, Graphics::DrawRectangle(IN const Pen,IN const Rect &), _gdiplus_CLASS_Graphics_DrawRectangle_Pen_pen_Rect_rect_, gdiplus._gdiplus_CLASS_Graphics_DrawRectangle_Pen_pen_Rect_rect_
ms.topic: method
f1_keywords: 
 - "gdiplusgraphics/Graphics.DrawRectangle"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Graphics.DrawRectangle
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# Graphics::DrawRectangle(IN const Pen,IN const Rect &)


## -description


The <b>Graphics::DrawRectangle</b> method draws a rectangle.


## -parameters




### -param pen [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>*</b>

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> that is used to draw a rectangle. 


### -param rect [in, ref]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a></b>

Reference to the rectangle to be drawn. 


## -returns



Type: <strong>Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangles(inconstpen_inconstrect_inint)">DrawRectangles Methods</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inconstrect_)">FillRectangle Methods</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-using-a-pen-to-draw-lines-and-rectangles-use">Using a Pen to Draw Lines and Rectangles</a>
 

 

