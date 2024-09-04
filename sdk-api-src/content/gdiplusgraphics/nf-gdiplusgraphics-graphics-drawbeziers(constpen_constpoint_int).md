---
UID: NF:gdiplusgraphics.Graphics.DrawBeziers(constPen,constPoint,INT)
title: Graphics::DrawBeziers(IN const Pen,IN const Point,IN INT) (gdiplusgraphics.h)
description: The Graphics::DrawBeziers method draws a sequence of connected Bézier splines.
helpviewer_keywords: ["DrawBeziers","DrawBeziers method [GDI+]","DrawBeziers method [GDI+]","Graphics class","Graphics class [GDI+]","DrawBeziers method","Graphics.DrawBeziers","Graphics.DrawBeziers(IN const Pen","IN const Point","IN INT)","Graphics.DrawBeziers(const Pen*","const Point*","INT)","Graphics::DrawBeziers","Graphics::DrawBeziers(IN const Pen","IN const Point","IN INT)","_gdiplus_CLASS_Graphics_DrawBeziers_Pen_pen_Point_points_INT_count_","gdiplus._gdiplus_CLASS_Graphics_DrawBeziers_Pen_pen_Point_points_INT_count_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawBeziers_Pen_pen_Point_points_INT_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawbeziersmethods\drawbeziers.htm
ms.date: 12/05/2018
ms.keywords: DrawBeziers, DrawBeziers method [GDI+], DrawBeziers method [GDI+],Graphics class, Graphics class [GDI+],DrawBeziers method, Graphics.DrawBeziers, Graphics.DrawBeziers(IN const Pen,IN const Point,IN INT), Graphics.DrawBeziers(const Pen*,const Point*,INT), Graphics::DrawBeziers, Graphics::DrawBeziers(IN const Pen,IN const Point,IN INT), _gdiplus_CLASS_Graphics_DrawBeziers_Pen_pen_Point_points_INT_count_, gdiplus._gdiplus_CLASS_Graphics_DrawBeziers_Pen_pen_Point_points_INT_count_
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
 - Graphics::DrawBeziers
 - gdiplusgraphics/Graphics::DrawBeziers
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
 - Graphics.DrawBeziers
---

# Graphics::DrawBeziers(IN const Pen,IN const Point,IN INT)


## -description

The <b>Graphics::DrawBeziers</b> method draws a sequence of connected Bézier splines.

## -parameters

### -param pen [in]

Type: <b>const <a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>*</b>

Pointer to a pen that is used to draw the Bézier splines.

### -param points [in]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>*</b>

Pointer to an array of <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a> objects that specify the starting, ending, and control points of the Bézier splines. The ending coordinate of one Bézier spline is the starting coordinate of the next Bézier spline.

### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the 
					<i>points</i> array.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

A Bézier spline does not pass through its control points. The control points act as magnets, pulling the curve in certain directions to influence the way the Bézier splines bend.


#### Examples



The following example draws a pair of Bézier curves.


```cpp

VOID Example_DrawBeziers(HDC hdc)
{
   Graphics graphics(hdc);

   // Define a Pen object and an array of Point objects.
   Pen greenPen(Color(255, 0, 255, 0), 3);

   Point startPoint(100, 100);
   Point ctrlPoint1(200, 50);
   Point ctrlPoint2(400, 10);
   Point endPoint1(500, 100);
   Point ctrlPoint3(600, 200);
   Point ctrlPoint4(700, 400);
   Point endPoint2(500, 500);

   Point curvePoints[7] = {
      startPoint,
      ctrlPoint1,
      ctrlPoint2,
      endPoint1,
      ctrlPoint3,
      ctrlPoint4,
      endPoint2};

   // Draw the Bezier curves.
   graphics.DrawBeziers(&greenPen, curvePoints, 7);

   // Draw the control and end points.
   SolidBrush redBrush(Color(255, 255, 0, 0));
   graphics.FillEllipse(&redBrush, Rect(100 - 5, 100 - 5, 10, 10));
   graphics.FillEllipse(&redBrush, Rect(500 - 5, 100 - 5, 10, 10));
   graphics.FillEllipse(&redBrush, Rect(500 - 5, 500 - 5, 10, 10));
   SolidBrush blueBrush(Color(255, 0, 0, 255));
   graphics.FillEllipse(&blueBrush, Rect(200 - 5, 50 - 5, 10, 10));
   graphics.FillEllipse(&blueBrush, Rect(400 - 5, 10 - 5, 10, 10));
   graphics.FillEllipse(&blueBrush, Rect(600 - 5, 200 - 5, 10, 10));
   graphics.FillEllipse(&blueBrush, Rect(700 - 5, 400 - 5, 10, 10));
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-bezier-splines-about">Bézier Splines</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inconstpointf__inconstpointf__inconstpointf__inconstpointf_)">DrawBezier Methods</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbeziers(inconstpen_inconstpoint_inint)">DrawBeziers</a>



<a href="/windows/desktop/gdiplus/-gdiplus-drawing-bezier-splines-use">Drawing Bézier Splines</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>