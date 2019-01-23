---
UID: NF:gdiplusgraphics.Graphics.DrawArc(IN const Pen,IN INT,IN INT,IN INT,IN INT,IN REAL,IN REAL)
title: Graphics::DrawArc(IN const Pen,IN INT,IN INT,IN INT,IN INT,IN REAL,IN REAL)
author: windows-sdk-content
description: The Graphics::DrawArc method draws an arc. The arc is part of an ellipse.
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawArc_Pen_pen_INT_x_INT_y_INT_width_INT_height_REAL_startAngle_REAL_sweepA.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawarcmethods\drawarc_40penpen_intx_inty_intwidth_intheight_re.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DrawArc, DrawArc method [GDI+], DrawArc method [GDI+],Graphics class, Graphics class [GDI+],DrawArc method, Graphics.DrawArc, Graphics.DrawArc(IN const Pen,IN INT,IN INT,IN INT,IN INT,IN REAL,IN REAL), Graphics.DrawArc(const Pen*,INT,INT,INT,INT,REAL,REAL), Graphics::DrawArc, Graphics::DrawArc(IN const Pen,IN INT,IN INT,IN INT,IN INT,IN REAL,IN REAL), _gdiplus_CLASS_Graphics_DrawArc_Pen_pen_INT_x_INT_y_INT_width_INT_height_REAL_startAngle_REAL_sweepA, gdiplus._gdiplus_CLASS_Graphics_DrawArc_Pen_pen_INT_x_INT_y_INT_width_INT_height_REAL_startAngle_REAL_sweepA
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

# Graphics::DrawArc(IN const Pen,IN INT,IN INT,IN INT,IN INT,IN REAL,IN REAL)


## -description


The <b>Graphics::DrawArc</b> method draws an arc. The arc is part of an ellipse.


## -parameters




### -param pen [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a>*</b>

Pointer to a pen that is used to draw the arc. 


### -param x [in]

Type: <b>INT</b>

Integer that specifies the x-coordinate of the upper-left corner of the bounding rectangle for the ellipse that contains the arc. 


### -param y [in]

Type: <b>INT</b>

Integer that specifies the y-coordinate of the upper-left corner of the bounding rectangle for the ellipse that contains the arc. 


### -param width [in]

Type: <b>INT</b>

Integer that specifies the width of the ellipse that contains the arc. 


### -param height [in]

Type: <b>INT</b>

Integer that specifies the height of the ellipse that contains the arc. 


### -param startAngle [in]

Type: <b>REAL</b>

Real number that specifies the angle between the x-axis and the starting point of the arc. 


### -param sweepAngle [in]

Type: <b>REAL</b>

Real number that specifies the angle between the starting and ending points of the arc. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Ok</a>, which is an element of the 
						<b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms533919(v=VS.85).aspx">Creating Figures from Lines, Curves, and Shapes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535733(v=VS.85).aspx">DrawArc Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535744(v=VS.85).aspx">DrawEllipse Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536362(v=VS.85).aspx">Ellipses and Arcs</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534495(v=VS.85).aspx">Rect</a>
 

 

