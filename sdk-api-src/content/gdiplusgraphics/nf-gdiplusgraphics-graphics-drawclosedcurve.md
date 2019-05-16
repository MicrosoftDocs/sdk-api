---
UID: NF:gdiplusgraphics.Graphics.DrawClosedCurve
title: Graphics::DrawClosedCurve
description: The Graphics::DrawClosedCurve method draws a closed cardinal spline.
ms.assetid: 49d14771-2cfb-4b42-b0cd-e8f9ef209b32
ms.author: windowssdkdev
ms.date: 05/13/2019
ms.keywords: Graphics::DrawClosedCurve
ms.topic: language-reference
targetos: Windows
product: Windows
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

Pointer to an array of <a href="https://msdn.microsoft.com/en-us/library/ms534488(v=VS.85).aspx">PointF</a> objects that specify the coordinates of the closed cardinal spline.
The array of <a href="https://msdn.microsoft.com/en-us/library/ms534488(v=VS.85).aspx">PointF</a> objects must contain a minimum of three elements.

### -param count

Integer that specifies the number of elements in the *points* array.

## -returns

If the method succeeds, it returns <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Ok</a>, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

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

<a href="https://msdn.microsoft.com/en-us/library/ms536358(v=VS.85).aspx">Cardinal Splines</a>

<a href="https://msdn.microsoft.com/en-us/library/ms535742(v=VS.85).aspx">DrawCurve Methods</a>

<a href="https://msdn.microsoft.com/en-us/library/ms533934(v=VS.85).aspx">Drawing Cardinal Splines</a>

<a href="https://msdn.microsoft.com/en-us/library/ms535765(v=VS.85).aspx">FillClosedCurve Methods</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534488(v=VS.85).aspx">PointF</a>
