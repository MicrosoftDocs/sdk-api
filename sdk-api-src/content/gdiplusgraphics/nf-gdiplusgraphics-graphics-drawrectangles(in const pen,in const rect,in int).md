---
UID: NF:gdiplusgraphics.Graphics.DrawRectangles(IN const Pen,IN const Rect,IN INT)
title: Graphics::DrawRectangles(IN const Pen,IN const Rect,IN INT)
author: windows-sdk-content
description: The Graphics::DrawRectangles method draws a sequence of rectangles.
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawRectangles_Pen_pen_Rect_rects_INT_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawrectanglesmethods\drawrectangles.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: DrawRectangles, DrawRectangles method [GDI+], DrawRectangles method [GDI+],Graphics class, Graphics class [GDI+],DrawRectangles method, Graphics.DrawRectangles, Graphics.DrawRectangles(IN const Pen,IN const Rect,IN INT), Graphics.DrawRectangles(const Pen*,const Rect*,INT), Graphics::DrawRectangles, Graphics::DrawRectangles(IN const Pen,IN const Rect,IN INT), _gdiplus_CLASS_Graphics_DrawRectangles_Pen_pen_Rect_rects_INT_count_, gdiplus._gdiplus_CLASS_Graphics_DrawRectangles_Pen_pen_Rect_rects_INT_count_
ms.prod: windows-hardware
ms.technology: windows-devices
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
---

# Graphics::DrawRectangles(IN const Pen,IN const Rect,IN INT)


## -description


The <b>Graphics::DrawRectangles</b> method draws a sequence of rectangles.


## -parameters




### -param pen [in]

Type: <b>const <a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> that is used to draw the rectangles. 


### -param rects [in]

Type: <b>const <a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a>*</b>

Pointer to an array of <a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a> objects that specify the coordinates of the rectangles to be drawn. 


### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the <i>rects</i> array. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/1c0c0e09-2304-4d68-9dd0-22b0861a2492">DrawRectangles Methods</a>



<a href="https://msdn.microsoft.com/91d3fc66-4c0d-4b44-beae-59f13b80483d">FillRectangle Methods</a>



<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>



<a href="https://msdn.microsoft.com/d91562ab-41e6-4bca-a320-74f490a4f88f">Pens, Lines, and Rectangles</a>



<a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a>



<a href="https://msdn.microsoft.com/f2e4144f-f2f1-49db-bfdf-ffce3023b4cb">Using a Pen to Draw Lines and Rectangles</a>
 

 

