---
UID: NF:gdiplusgraphics.Graphics.DrawPie(constPen,INT,INT,INT,INT,REAL,REAL)
title: Graphics::DrawPie(IN const Pen,IN INT,IN INT,IN INT,IN INT,IN REAL,IN REAL) (gdiplusgraphics.h)
description: The Graphics::DrawPie method draws a pie. (overload 3/4)
helpviewer_keywords: ["DrawPie","DrawPie method [GDI+]","DrawPie method [GDI+]","Graphics class","Graphics class [GDI+]","DrawPie method","Graphics.DrawPie","Graphics.DrawPie(IN const Pen","IN INT","IN INT","IN INT","IN INT","IN REAL","IN REAL)","Graphics.DrawPie(const Pen*","INT","INT","INT","INT","REAL","REAL)","Graphics::DrawPie","Graphics::DrawPie(IN const Pen","IN INT","IN INT","IN INT","IN INT","IN REAL","IN REAL)","_gdiplus_CLASS_Graphics_DrawPie_Pen_pen_INT_x_INT_y_INT_width_INT_height_REAL_startAngle_REAL_sweepA","gdiplus._gdiplus_CLASS_Graphics_DrawPie_Pen_pen_INT_x_INT_y_INT_width_INT_height_REAL_startAngle_REAL_sweepA"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawPie_Pen_pen_INT_x_INT_y_INT_width_INT_height_REAL_startAngle_REAL_sweepA.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawpiemethods\drawpie_2penpen_intx_inty_intwidth_intheight_rea.htm
ms.date: 12/05/2018
ms.keywords: DrawPie, DrawPie method [GDI+], DrawPie method [GDI+],Graphics class, Graphics class [GDI+],DrawPie method, Graphics.DrawPie, Graphics.DrawPie(IN const Pen,IN INT,IN INT,IN INT,IN INT,IN REAL,IN REAL), Graphics.DrawPie(const Pen*,INT,INT,INT,INT,REAL,REAL), Graphics::DrawPie, Graphics::DrawPie(IN const Pen,IN INT,IN INT,IN INT,IN INT,IN REAL,IN REAL), _gdiplus_CLASS_Graphics_DrawPie_Pen_pen_INT_x_INT_y_INT_width_INT_height_REAL_startAngle_REAL_sweepA, gdiplus._gdiplus_CLASS_Graphics_DrawPie_Pen_pen_INT_x_INT_y_INT_width_INT_height_REAL_startAngle_REAL_sweepA
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - Graphics::DrawPie
 - gdiplusgraphics/Graphics::DrawPie
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Graphics.DrawPie
---

# Graphics::DrawPie(IN const Pen,IN INT,IN INT,IN INT,IN INT,IN REAL,IN REAL)


## -description

The <b>Graphics::DrawPie</b> method draws a pie.

## -parameters

### -param pen [in]

Type: <b>const <a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>*</b>

Pointer to a pen that is used to draw the pie.

### -param x [in]

Type: <b>INT</b>

Integer that specifies the x-coordinate of the upper-left corner of the rectangle that bounds the ellipse in which to draw the pie.

### -param y [in]

Type: <b>INT</b>

Integer that specifies the y-coordinate of the upper-left corner of the rectangle that bounds the ellipse in which to draw the pie.

### -param width [in]

Type: <b>INT</b>

Integer that specifies the width of the rectangle that bounds the ellipse in which to draw the pie.

### -param height [in]

Type: <b>INT</b>

Integer that specifies the height of the rectangle that bounds the ellipse in which to draw the pie.

### -param startAngle [in]

Type: <b>REAL</b>

Real number that specifies the angle, in degrees, between the x-axis and the starting point of the arc that defines the pie. A positive value specifies clockwise rotation.

### -param sweepAngle [in]

Type: <b>REAL</b>

Real number that specifies the angle, in degrees, between the starting and ending points of the arc that defines the pie. A positive value specifies clockwise rotation.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

The following illustration shows the pie that is drawn in the ellipse that is bounded by the rectangle. The illustration also shows the horizontal axis of the ellipse and the direction of the 
				<i>startAngle</i> and the <i>sweepAngle</i>.

<img alt="Illustration showing an ellipse with an outlined pie; the start angle and sweep angle are labeled" src="images/drawpie1.png"/>

#### Examples



The following example draws a pie.


```cpp

VOID Example_DrawPie3(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a Pen object.
   Pen blackPen(Color(255, 0, 0, 0), 3);

   // Define the pie.
   int x = 0;
   int y = 0;
   int width = 200;
   int height = 100;
   REAL startAngle = 0.0f;
   REAL sweepAngle = 45.0f;

   // Draw the pie.
   graphics.DrawPie(&blackPen, x, y, width, height, startAngle, sweepAngle);
}

```

## -see-also

<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inconstrect__inreal_inreal)">FillPie Methods</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/gdiplus/-gdiplus-open-and-closed-curves-about">Open and Closed Curves</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>
