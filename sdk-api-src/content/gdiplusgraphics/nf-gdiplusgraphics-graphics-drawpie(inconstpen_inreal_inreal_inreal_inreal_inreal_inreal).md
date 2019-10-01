---
UID: NF:gdiplusgraphics.Graphics.DrawPie(IN const Pen,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL)
title: Graphics::DrawPie(IN const Pen,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL) (gdiplusgraphics.h)
author: windows-sdk-content
description: The Graphics::DrawPie method draws a pie.
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawPie_Pen_pen_REAL_x_REAL_y_REAL_width_REAL_height_REAL_startAngle_REAL_sw.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawpiemethods\drawpie_2penpen_realx_realy_realwidth_realheight.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DrawPie, DrawPie method [GDI+], DrawPie method [GDI+],Graphics class, Graphics class [GDI+],DrawPie method, Graphics.DrawPie, Graphics.DrawPie(IN const Pen,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL), Graphics.DrawPie(const Pen*,REAL,REAL,REAL,REAL,REAL,REAL), Graphics::DrawPie, Graphics::DrawPie(IN const Pen,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL), _gdiplus_CLASS_Graphics_DrawPie_Pen_pen_REAL_x_REAL_y_REAL_width_REAL_height_REAL_startAngle_REAL_sw, gdiplus._gdiplus_CLASS_Graphics_DrawPie_Pen_pen_REAL_x_REAL_y_REAL_width_REAL_height_REAL_startAngle_REAL_sw
ms.topic: method
f1_keywords: 
 - "gdiplusgraphics/Graphics.DrawPie"
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# Graphics::DrawPie(IN const Pen,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL)


## -description


The <b>Graphics::DrawPie</b> method draws a pie.


## -parameters




### -param pen [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>*</b>

Pointer to a pen that is used to draw the pie. 


### -param x [in]

Type: <b>REAL</b>

Real number that specifies the x-coordinate of the upper-left corner of the rectangle that bounds the ellipse in which to draw the pie. 


### -param y [in]

Type: <b>REAL</b>

Real number that specifies the y-coordinate of the upper-left corner of the rectangle that bounds the ellipse in which to draw the pie. 


### -param width [in]

Type: <b>REAL</b>

Real number that specifies the width of the rectangle that bounds the ellipse in which to draw the pie. 


### -param height [in]

Type: <b>REAL</b>

Real number that specifies the height of the rectangle that bounds the ellipse in which to draw the pie. 


### -param startAngle [in]

Type: <b>REAL</b>

Real number that specifies the angle, in degrees, between the x-axis and the starting point of the arc that defines the pie. A positive value specifies clockwise rotation. 


### -param sweepAngle [in]

Type: <b>REAL</b>

Real number that specifies the angle, in degrees, between the starting and ending points of the arc that defines the pie. A positive value specifies clockwise rotation. 


## -returns



Type: <strong>Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.




## -remarks



The following illustration shows the pie that is drawn in the ellipse that is bounded by the rectangle. The illustration also shows the horizontal axis of the ellipse and the direction of the 
				<i>startAngle</i> and the <i>sweepAngle</i>.

<img alt="Illustration showing an ellipse with an outlined pie; the start angle and sweep angle are labeled" src="images/drawpie1.png"/>

#### Examples



The following example draws a pie.


```cpp
VOID Example_DrawPie4(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a Pen object.
   Pen blackPen(Color(255, 0, 0, 0), 3);

   // Define the pie.
   REAL x = 0.0f;
   REAL y = 0.0f;
   REAL width = 200.0f;
   REAL height = 100.0f;
   REAL startAngle = 0.0f;
   REAL sweepAngle = 45.0f;

   // Draw the pie.
   graphics.DrawPie(&blackPen, x, y, width, height, startAngle, sweepAngle);
}

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inconstrect__inreal_inreal)">FillPie Methods</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-open-and-closed-curves-about">Open and Closed Curves</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a>
 

 

