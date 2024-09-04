---
UID: NF:gdiplusgraphics.Graphics.DrawBezier(constPen,INT,INT,INT,INT,INT,INT,INT,INT)
title: Graphics::DrawBezier(IN const Pen,IN INT,IN INT,IN INT,IN INT,IN INT,IN INT,IN INT,IN INT) (gdiplusgraphics.h)
description: The Graphics::DrawBezier method draws a Bézier spline. (overload 2/3)
helpviewer_keywords: ["DrawBezier","DrawBezier method [GDI+]","DrawBezier method [GDI+]","Graphics class","Graphics class [GDI+]","DrawBezier method","Graphics.DrawBezier","Graphics.DrawBezier(IN const Pen","IN INT","IN INT","IN INT","IN INT","IN INT","IN INT","IN INT","IN INT)","Graphics.DrawBezier(const Pen*","INT","INT","INT","INT","INT","INT","INT","INT)","Graphics::DrawBezier","Graphics::DrawBezier(IN const Pen","IN INT","IN INT","IN INT","IN INT","IN INT","IN INT","IN INT","IN INT)","_gdiplus_CLASS_Graphics_DrawBezier_Pen_pen_INT_x1_INT_y1_INT_x2_INT_y2_INT_x3_INT_y3_INT_x4_INT_y4_","gdiplus._gdiplus_CLASS_Graphics_DrawBezier_Pen_pen_INT_x1_INT_y1_INT_x2_INT_y2_INT_x3_INT_y3_INT_x4_INT_y4_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawBezier_Pen_pen_INT_x1_INT_y1_INT_x2_INT_y2_INT_x3_INT_y3_INT_x4_INT_y4_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawbeziermethods\drawbezier_76penpen_intx1_inty1_intx2_inty2_intx3_i.htm
ms.date: 12/05/2018
ms.keywords: DrawBezier, DrawBezier method [GDI+], DrawBezier method [GDI+],Graphics class, Graphics class [GDI+],DrawBezier method, Graphics.DrawBezier, Graphics.DrawBezier(IN const Pen,IN INT,IN INT,IN INT,IN INT,IN INT,IN INT,IN INT,IN INT), Graphics.DrawBezier(const Pen*,INT,INT,INT,INT,INT,INT,INT,INT), Graphics::DrawBezier, Graphics::DrawBezier(IN const Pen,IN INT,IN INT,IN INT,IN INT,IN INT,IN INT,IN INT,IN INT), _gdiplus_CLASS_Graphics_DrawBezier_Pen_pen_INT_x1_INT_y1_INT_x2_INT_y2_INT_x3_INT_y3_INT_x4_INT_y4_, gdiplus._gdiplus_CLASS_Graphics_DrawBezier_Pen_pen_INT_x1_INT_y1_INT_x2_INT_y2_INT_x3_INT_y3_INT_x4_INT_y4_
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
 - Graphics::DrawBezier
 - gdiplusgraphics/Graphics::DrawBezier
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
 - Graphics.DrawBezier
---

# Graphics::DrawBezier(IN const Pen,IN INT,IN INT,IN INT,IN INT,IN INT,IN INT,IN INT,IN INT)


## -description

The <b>Graphics::DrawBezier</b> method draws a Bézier spline.

## -parameters

### -param pen [in]

Type: <b>const <a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>*</b>

Pointer to a pen that is used to draw the Bézier spline.

### -param x1 [in]

Type: <b>INT</b>

Integer that specifies the x-coordinate of the starting point of the Bézier spline.

### -param y1 [in]

Type: <b>INT</b>

Integer that specifies the y-coordinate of the starting point of the Bézier spline.

### -param x2 [in]

Type: <b>INT</b>

Integer that specifies the x-coordinate of the first control point of the Bézier spline.

### -param y2 [in]

Type: <b>INT</b>

Integer that specifies the y-coordinate of the first control point of the Bézier spline

### -param x3 [in]

Type: <b>INT</b>

Integer that specifies the x-coordinate of the second control point of the Bézier spline.

### -param y3 [in]

Type: <b>INT</b>

Integer that specifies the y-coordinate of the second control point of the Bézier spline.

### -param x4 [in]

Type: <b>INT</b>

Integer that specifies the x-coordinate of the ending point of the Bézier spline.

### -param y4 [in]

Type: <b>INT</b>

Integer that specifies the y-coordinate of the ending point of the Bézier spline

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

A Bézier spline does not pass through its control points. The control points act as magnets, pulling the curve in certain directions to influence the way the Bézier spline bends.


#### Examples



The following example draws a Bézier curve.


```cpp

VOID Example_DrawBezier3(HDC hdc)
{
   Graphics graphics(hdc);

   // Set up the pen and curve points.
   Pen greenPen(Color(255, 0, 255, 0));
   int startPointx = 100;
   int startPointy = 100;
   int ctrlPoint1x = 200;
   int ctrlPoint1y = 10;
   int ctrlPoint2x = 350;
   int ctrlPoint2y = 50;
   int endPointx = 500;
   int endPointy = 100;

   //Draw the curve.
   graphics.DrawBezier(
   &greenPen,
   startPointx,
   startPointy,
   ctrlPoint1x,
   ctrlPoint1y,
   ctrlPoint2x,
   ctrlPoint2y,
   endPointx,
   endPointy);

   //Draw the end points and control points.
   SolidBrush redBrush(Color(255, 255, 0, 0));
   SolidBrush blueBrush(Color(255, 0, 0, 255));
   graphics.FillEllipse(&redBrush, 100 - 5, 100 - 5, 10, 10);
   graphics.FillEllipse(&redBrush, 500 - 5, 100 - 5, 10, 10);
   graphics.FillEllipse(&blueBrush, 200 - 5, 10 - 5, 10, 10);
   graphics.FillEllipse(&blueBrush, 350 - 5, 50 - 5, 10, 10);
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-bezier-splines-about">Bézier Splines</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inconstpointf__inconstpointf__inconstpointf__inconstpointf_)">DrawBezier</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbeziers(inconstpen_inconstpoint_inint)">DrawBeziers Methods</a>



<a href="/windows/desktop/gdiplus/-gdiplus-drawing-bezier-splines-use">Drawing Bézier Splines</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>
