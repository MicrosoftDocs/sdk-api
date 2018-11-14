---
UID: NF:gdiplusgraphics.Graphics.DrawEllipse(IN const Pen,IN REAL,IN REAL,IN REAL,IN REAL)
title: Graphics::DrawEllipse(IN const Pen,IN REAL,IN REAL,IN REAL,IN REAL)
author: windows-sdk-content
description: The Graphics::DrawEllipse method draws an ellipse.
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawEllipse_Pen_pen_REAL_x_REAL_y_REAL_width_REAL_height_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawellipsemethods\drawellipse_58penpen_realx_realy_realwidth_realheigh.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: DrawEllipse, DrawEllipse method [GDI+], DrawEllipse method [GDI+],Graphics class, Graphics class [GDI+],DrawEllipse method, Graphics.DrawEllipse, Graphics.DrawEllipse(IN const Pen,IN REAL,IN REAL,IN REAL,IN REAL), Graphics.DrawEllipse(const Pen*,REAL,REAL,REAL,REAL), Graphics::DrawEllipse, Graphics::DrawEllipse(IN const Pen,IN REAL,IN REAL,IN REAL,IN REAL), _gdiplus_CLASS_Graphics_DrawEllipse_Pen_pen_REAL_x_REAL_y_REAL_width_REAL_height_, gdiplus._gdiplus_CLASS_Graphics_DrawEllipse_Pen_pen_REAL_x_REAL_y_REAL_width_REAL_height_
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
 - Graphics.DrawEllipse
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- gdiplusgraphics.h
: 
- Graphics.DrawEllipse
: 
req.product: GDI+ 1.0
---

# Graphics::DrawEllipse(IN const Pen,IN REAL,IN REAL,IN REAL,IN REAL)


## -description


The <b>Graphics::DrawEllipse</b> method draws an ellipse.


## -parameters




### -param pen [in]

Type: <b>const <a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>*</b>

Pointer to a pen that is used to draw the ellipse. 


### -param x [in]

Type: <b>REAL</b>

Real number that specifies the x-coordinate of the upper-left corner of the rectangle that bounds the ellipse. 


### -param y [in]

Type: <b>REAL</b>

Real number that specifies the y-coordinate of the upper-left corner of the rectangle that bounds the ellipse. 


### -param width [in]

Type: <b>REAL</b>

Real number that specifies the width of the rectangle that bounds the ellipse. 


### -param height [in]

Type: <b>REAL</b>

Real number that specifies the height of the rectangle that bounds the ellipse. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/45e80501-4d64-480b-a7c7-3af52c00a0aa">Ellipses and Arcs</a>



<a href="https://msdn.microsoft.com/92f6f3ca-337b-4f57-9472-2dc677550b39">FillEllipse Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>



<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>
 

 

