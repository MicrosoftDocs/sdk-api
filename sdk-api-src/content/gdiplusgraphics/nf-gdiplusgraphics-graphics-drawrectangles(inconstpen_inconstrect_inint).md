---
UID: NF:gdiplusgraphics.Graphics.DrawRectangles(IN const Pen,IN const Rect,IN INT)
title: Graphics::DrawRectangles(IN const Pen,IN const Rect,IN INT) (gdiplusgraphics.h)
author: windows-sdk-content
description: The Graphics::DrawRectangles method draws a sequence of rectangles.
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawRectangles_Pen_pen_Rect_rects_INT_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawrectanglesmethods\drawrectangles.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DrawRectangles, DrawRectangles method [GDI+], DrawRectangles method [GDI+],Graphics class, Graphics class [GDI+],DrawRectangles method, Graphics.DrawRectangles, Graphics.DrawRectangles(IN const Pen,IN const Rect,IN INT), Graphics.DrawRectangles(const Pen*,const Rect*,INT), Graphics::DrawRectangles, Graphics::DrawRectangles(IN const Pen,IN const Rect,IN INT), _gdiplus_CLASS_Graphics_DrawRectangles_Pen_pen_Rect_rects_INT_count_, gdiplus._gdiplus_CLASS_Graphics_DrawRectangles_Pen_pen_Rect_rects_INT_count_
ms.topic: method
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
 - Graphics.DrawRectangles
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# Graphics::DrawRectangles(IN const Pen,IN const Rect,IN INT)


## -description


The <b>Graphics::DrawRectangles</b> method draws a sequence of rectangles.


## -parameters




### -param pen [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>*</b>

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> that is used to draw the rectangles. 


### -param rects [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>*</b>

Pointer to an array of <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a> objects that specify the coordinates of the rectangles to be drawn. 


### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the <i>rects</i> array. 


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
 

 

