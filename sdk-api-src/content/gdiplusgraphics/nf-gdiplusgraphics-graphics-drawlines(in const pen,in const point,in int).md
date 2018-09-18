---
UID: NF:gdiplusgraphics.Graphics.DrawLines(IN const Pen,IN const Point,IN INT)
title: Graphics::DrawLines(IN const Pen,IN const Point,IN INT)
author: windows-sdk-content
description: The Graphics::DrawLines method draws a sequence of connected lines.
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawLines_Pen_pen_PointF_points_INT_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawlinesmethods\drawlines_39penpen_pointfpoints_intcount.htm
ms.author: windowssdkdev
ms.date: 09/12/2018
ms.keywords: DrawLines, DrawLines method [GDI+], DrawLines method [GDI+],Graphics class, Graphics class [GDI+],DrawLines method, Graphics.DrawLines, Graphics.DrawLines(IN const Pen,IN const Point,IN INT), Graphics.DrawLines(const Pen*,const PointF*,INT), Graphics::DrawLines, Graphics::DrawLines(IN const Pen,IN const Point,IN INT), _gdiplus_CLASS_Graphics_DrawLines_Pen_pen_PointF_points_INT_count_, gdiplus._gdiplus_CLASS_Graphics_DrawLines_Pen_pen_PointF_points_INT_count_
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
 - Graphics.DrawLines
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Graphics::DrawLines(IN const Pen,IN const Point,IN INT)


## -description


The <b>Graphics::DrawLines</b> method draws a sequence of connected lines.


## -parameters




### -param pen [in]

Type: <b>const <a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>*</b>

Pointer to a pen that is used to draw the lines. 


### -param points [in]

Type: <b>const <a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a>*</b>

Pointer to an array of <a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a> objects that specify the starting and ending points of the lines. 


### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the 
					<i>points</i> array. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/15c1c3fd-4479-46ad-a70c-f7d15bc69488">DrawLine Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>



<a href="https://msdn.microsoft.com/d91562ab-41e6-4bca-a320-74f490a4f88f">Pens, Lines, and Rectangles</a>



<a href="https://msdn.microsoft.com/8bf4d566-b061-4102-8307-218431e286f8">Point</a>



<a href="https://msdn.microsoft.com/f2e4144f-f2f1-49db-bfdf-ffce3023b4cb">Using a Pen to Draw Lines and Rectangles</a>
 

 

