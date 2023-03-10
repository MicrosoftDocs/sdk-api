---
UID: NF:gdiplusgraphics.Graphics.DrawClosedCurve(constPen,constPointF,INT)
title: Graphics::DrawClosedCurve
description: The Graphics::DrawClosedCurve method draws a closed cardinal spline. (overload 3/4)
tech.root: gdiplus
helpviewer_keywords: ["Graphics::DrawClosedCurve"]
ms.assetid: 49d14771-2cfb-4b42-b0cd-e8f9ef209b32
ms.date: 05/13/2019
ms.keywords: Graphics::DrawClosedCurve
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: gdiplusgraphics.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - Graphics::DrawClosedCurve
 - gdiplusgraphics/Graphics::DrawClosedCurve
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdiplusgraphics.h
api_name:
 - Graphics::DrawClosedCurve
---

# DrawClosedCurve(Pen*,PointF*,INT)


## -description

The **Graphics::DrawClosedCurve** method draws a closed cardinal spline.

## -parameters

### -param pen

Pointer to a pen that is used to draw the closed cardinal spline.

### -param points

Pointer to an array of <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a> objects that specify the coordinates of the closed cardinal spline.
The array of <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a> objects must contain a minimum of three elements.

### -param count

Integer that specifies the number of elements in the *points* array.

## -returns

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the **Status** enumeration.

## -remarks

Each ending point is the starting point for the next cardinal spline. 
In a closed cardinal spline, the curve continues through the last point in the *points* array and connects with the first point in the array.

#### Examples

The following example draws a closed cardinal spline.

```cpp
VOID Example_DrawClosedCurve3(HDC hdc)
{
   Graphics graphics(hdc);

   // Define a Pen object and an array of PointF objects.
   Pen greenPen(Color(255, 0, 0, 255), 3);
   PointF point1(100.0f, 100.0f);
   PointF point2(200.0f, 50.0f);
   PointF point3(400.0f, 10.0f);
   PointF point4(500.0f, 100.0f);
   PointF point5(600.0f, 200.0f);
   PointF point6(700.0f, 400.0f);
   PointF point7(500.0f, 500.0f);

   PointF curvePoints[7] = {
      point1,
      point2,
      point3,
      point4,
      point5,
      point6,
      point7};

   // Draw the closed curve.
   graphics.DrawClosedCurve(&greenPen, curvePoints, 7);

   // Draw the points in the curve.
   SolidBrush redBrush(Color(255, 255, 0, 0));
   graphics.FillEllipse(&redBrush, Rect(95, 95, 10, 10));
   graphics.FillEllipse(&redBrush, Rect(495, 95, 10, 10));
   graphics.FillEllipse(&redBrush, Rect(495, 495, 10, 10));
   graphics.FillEllipse(&redBrush, Rect(195, 45, 10, 10));
   graphics.FillEllipse(&redBrush, Rect(395, 5, 10, 10));
   graphics.FillEllipse(&redBrush, Rect(595, 195, 10, 10));
   graphics.FillEllipse(&redBrush, Rect(695, 395, 10, 10));
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-cardinal-splines-about">Cardinal Splines</a>

<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcurve(inconstpen_inconstpointf_inint_inint_inint_inreal)">DrawCurve Methods</a>

<a href="/windows/desktop/gdiplus/-gdiplus-drawing-cardinal-splines-use">Drawing Cardinal Splines</a>

<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpointf_inint_infillmode_inreal)">FillClosedCurve Methods</a>

<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>

<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a>
