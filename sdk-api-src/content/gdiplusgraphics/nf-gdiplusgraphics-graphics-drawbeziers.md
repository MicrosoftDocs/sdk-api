---
UID: NF:gdiplusgraphics.Graphics.DrawBeziers
title: Graphics::DrawBeziers
description: The Graphics::DrawBeziers method draws a sequence of connected Bezier splines.
ms.assetid: 3a0f5b23-24bb-4255-a6fe-30cfb701350a
ms.author: windowssdkdev
ms.date: 05/13/2019
ms.keywords: Graphics::DrawBeziers
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
 - Graphics::DrawBeziers
---

# DrawBeziers(Pen*,PointF*,INT)

## -description

The **Graphics::DrawBeziers** method draws a sequence of connected Bézier splines.

## -parameters

### -param pen

Pointer to a pen that is used to draw the Bézier splines.

### -param points

Pointer to an array of <a href="https://msdn.microsoft.com/en-us/library/ms534488(v=VS.85).aspx">PointF</a> objects that specify the starting, ending, and control points of the Bézier splines.

### -param count

Integer that specifies the number of elements in the *points* array.

## -returns

If the method succeeds, it returns <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Ok</a>, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the **Status** enumeration.

## -remarks

A Bézier spline does not pass through its control points.
The control points act as magnets, pulling the curve in certain directions to influence the way a Bézier spline bends.
Each Bézier spline requires a starting point and an ending point.
Each ending point is the starting point for the next Bézier spline.

#### Examples

The following example draws a pair of Bézier curves.

```cpp
VOID Example_DrawBeziers2(HDC hdc)
{
   Graphics graphics(hdc);

   // Define a Pen object and an array of PointF objects.
   Pen greenPen(Color(255, 0, 255, 0), 3);

   PointF startPoint(100.0f, 100.0f);
   PointF ctrlPoint1(200.0f, 50.0f);
   PointF ctrlPoint2(400.0f, 10.0f);
   PointF endPoint1(500.0f, 100.0f);
   PointF ctrlPoint3(600.0f, 200.0f);
   PointF ctrlPoint4(700.0f, 400.0f);
   PointF endPoint2(500.0f, 500.0f);

   PointF curvePoints[7] = {
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

<a href="https://msdn.microsoft.com/en-us/library/ms536354(v=VS.85).aspx">Bézier Splines</a>

<a href="https://msdn.microsoft.com/en-us/library/ms535734(v=VS.85).aspx">DrawBezier Methods</a>

<a href="https://msdn.microsoft.com/en-us/library/ms533926(v=VS.85).aspx">Drawing Bézier Splines</a>

<a href="https://msdn.microsoft.com/en-us/library/ms535738(v=VS.85).aspx">DrawBeziers</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534488(v=VS.85).aspx">PointF</a>
