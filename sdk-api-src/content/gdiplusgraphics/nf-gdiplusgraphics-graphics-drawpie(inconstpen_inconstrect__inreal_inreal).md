---
UID: NF:gdiplusgraphics.Graphics.DrawPie(IN const Pen,IN const Rect &,IN REAL,IN REAL)
title: Graphics::DrawPie(IN const Pen,IN const Rect &,IN REAL,IN REAL) (gdiplusgraphics.h)
author: windows-sdk-content
description: The Graphics::DrawPie method draws a pie.
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawPie_Pen_pen_Rect_rect_REAL_startAngle_REAL_sweepAngle_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawpiemethods\drawpie.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DrawPie, DrawPie method [GDI+], DrawPie method [GDI+],Graphics class, Graphics class [GDI+],DrawPie method, Graphics.DrawPie, Graphics.DrawPie(IN const Pen,IN const Rect &,IN REAL,IN REAL), Graphics.DrawPie(const Pen*,const Rect&,REAL,REAL), Graphics::DrawPie, Graphics::DrawPie(IN const Pen,IN const Rect &,IN REAL,IN REAL), _gdiplus_CLASS_Graphics_DrawPie_Pen_pen_Rect_rect_REAL_startAngle_REAL_sweepAngle_, gdiplus._gdiplus_CLASS_Graphics_DrawPie_Pen_pen_Rect_rect_REAL_startAngle_REAL_sweepAngle_
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
 - Graphics.DrawPie
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# Graphics::DrawPie(IN const Pen,IN const Rect &,IN REAL,IN REAL)


## -description


The <b>Graphics::DrawPie</b> method draws a pie.


## -parameters




### -param pen [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a>*</b>

Pointer to a pen that is used to draw the pie. 


### -param rect [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534495(v=VS.85).aspx">Rect</a></b>

Reference to a rectangle that bounds the ellipse in which to draw the pie. 


### -param startAngle [in]

Type: <b>REAL</b>

Real number that specifies the angle, in degrees, between the x-axis and the starting point of the arc that defines the pie. A positive value specifies clockwise rotation. 


### -param sweepAngle [in]

Type: <b>REAL</b>

Real number that specifies the angle, in degrees, between the starting and ending points of the arc that defines the pie. A positive value specifies clockwise rotation. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -remarks



The following illustration shows the pie that is drawn in the ellipse that is bounded by the rectangle. The illustration also shows the horizontal axis of the ellipse and the direction of the <i>startAngle</i> and the <i>sweepAngle</i>.

<img alt="Illustration showing an ellipse with an outlined pie; the start angle and sweep angle are labeled" src="images/drawpie1.png"/>

#### Examples



The following example draws a pie.


```cpp

VOID Example_DrawPie(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a Pen object.
   Pen blackPen(Color(255, 0, 0, 0), 3);

   // Define the pie.
   Rect ellipseRect(0, 0, 200, 100);
   REAL startAngle = 0.0f;
   REAL sweepAngle = 45.0f;

   // Draw the pie.
   graphics.DrawPie(&blackPen, ellipseRect, startAngle, sweepAngle);
}

```





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms535749(v=VS.85).aspx">DrawLines Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535769(v=VS.85).aspx">FillPie Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536366(v=VS.85).aspx">Open and Closed Curves</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534495(v=VS.85).aspx">Rect</a>
 

 

