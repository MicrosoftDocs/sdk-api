---
UID: NF:gdiplusgraphics.Graphics.DrawArc(IN const Pen,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL)
title: Graphics::DrawArc(IN const Pen,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL)
author: windows-sdk-content
description: The Graphics::DrawArc method draws an arc. The arc is part of an ellipse.
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawArc_Pen_pen_REAL_x_REAL_y_REAL_width_REAL_height_REAL_startAngle_REAL_sw.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawarcmethods\drawarc_29penpen_realx_realy_realwidth_realheigh.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: DrawArc, DrawArc method [GDI+], DrawArc method [GDI+],Graphics class, Graphics class [GDI+],DrawArc method, Graphics.DrawArc, Graphics.DrawArc(IN const Pen,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL), Graphics.DrawArc(const Pen*,REAL,REAL,REAL,REAL,REAL,REAL), Graphics::DrawArc, Graphics::DrawArc(IN const Pen,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL), _gdiplus_CLASS_Graphics_DrawArc_Pen_pen_REAL_x_REAL_y_REAL_width_REAL_height_REAL_startAngle_REAL_sw, gdiplus._gdiplus_CLASS_Graphics_DrawArc_Pen_pen_REAL_x_REAL_y_REAL_width_REAL_height_REAL_startAngle_REAL_sw
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
 - Graphics.DrawArc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Graphics::DrawArc(IN const Pen,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL)


## -description


The <b>Graphics::DrawArc</b> method draws an arc. The arc is part of an ellipse.


## -parameters




### -param pen [in]

Type: <b>const <a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>*</b>

Pointer to a pen that is used to draw the arc. 


### -param x [in]

Type: <b>REAL</b>

Real number that specifies the x-coordinate of the upper-left corner of the bounding rectangle for the ellipse that contains the arc. 


### -param y [in]

Type: <b>REAL</b>

Real number that specifies the y-coordinate of the upper-left corner of the bounding rectangle for the ellipse that contains the arc. 


### -param width [in]

Type: <b>REAL</b>

Real number that specifies the width of the ellipse that contains the arc. 


### -param height [in]

Type: <b>REAL</b>

Real number that specifies the height of the ellipse that contains the arc. 


### -param startAngle [in]

Type: <b>REAL</b>

Real number that specifies the angle between the x-axis and the starting point of the arc. 


### -param sweepAngle [in]

Type: <b>REAL</b>

Real number that specifies the angle between the starting and ending points of the arc. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Ok</a>, which is an element of the 
						<b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/66faeb73-16fb-4b7f-a4d5-a90ec2590d8c">Creating Figures from Lines, Curves, and Shapes</a>



<a href="https://msdn.microsoft.com/b30757ea-b8b8-45bd-a716-a4c8c9c5f1ec">DrawArc Methods</a>



<a href="https://msdn.microsoft.com/1abaee7d-63a5-4786-b08c-f3b59e50f180">DrawEllipse Methods</a>



<a href="https://msdn.microsoft.com/45e80501-4d64-480b-a7c7-3af52c00a0aa">Ellipses and Arcs</a>



<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>



<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>



<a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a>
 

 

