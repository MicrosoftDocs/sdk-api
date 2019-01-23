---
UID: NF:gdiplusgraphics.Graphics.DrawLine(IN const Pen,IN INT,IN INT,IN INT,IN INT)
title: Graphics::DrawLine(IN const Pen,IN INT,IN INT,IN INT,IN INT)
author: windows-sdk-content
description: The Graphics::DrawLine method draws a line that connects two points.
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawLine_Pen_pen_INT_x1_INT_y1_INT_x2_INT_y2_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawlinemethods\drawline_67penpen_intx1_inty1_intx2_inty2.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DrawLine, DrawLine method [GDI+], DrawLine method [GDI+],Graphics class, Graphics class [GDI+],DrawLine method, Graphics.DrawLine, Graphics.DrawLine(IN const Pen,IN INT,IN INT,IN INT,IN INT), Graphics.DrawLine(const Pen*,INT,INT,INT,INT), Graphics::DrawLine, Graphics::DrawLine(IN const Pen,IN INT,IN INT,IN INT,IN INT), _gdiplus_CLASS_Graphics_DrawLine_Pen_pen_INT_x1_INT_y1_INT_x2_INT_y2_, gdiplus._gdiplus_CLASS_Graphics_DrawLine_Pen_pen_INT_x1_INT_y1_INT_x2_INT_y2_
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
 - Graphics.DrawLine
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Graphics::DrawLine(IN const Pen,IN INT,IN INT,IN INT,IN INT)


## -description


The <b>Graphics::DrawLine</b> method draws a line that connects two points.


## -parameters




### -param pen [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a>*</b>

Pointer to a pen that is used to draw the line. 


### -param x1 [in]

Type: <b>INT</b>

Integer that specifies the x-coordinate of the starting point of the line. 


### -param y1 [in]

Type: <b>INT</b>

Integer that specifies the y-coordinate of the starting point of the line. 


### -param x2 [in]

Type: <b>INT</b>

Integer that specifies the x-coordinate of the ending point of the line. 


### -param y2 [in]

Type: <b>INT</b>

Integer that specifies the y-coordinate of the ending point of the line. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the 
						<b>Status</b> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms535749(v=VS.85).aspx">DrawLines Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536372(v=VS.85).aspx">Pens, Lines, and Rectangles</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534487(v=VS.85).aspx">Point</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533855(v=VS.85).aspx">Using a Pen to Draw Lines and Rectangles</a>
 

 

