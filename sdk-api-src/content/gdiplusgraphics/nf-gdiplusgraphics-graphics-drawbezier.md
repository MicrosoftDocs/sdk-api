---
UID: NF:gdiplusgraphics.Graphics.DrawBezier
title: Graphics::DrawBezier
description: The Graphics::DrawBezier method draws a Bezier spline.
ms.assetid: 8cc50b20-3c78-4462-bee5-f7fce4815bc1
ms.author: windowssdkdev
ms.date: 05/13/2019
ms.keywords: Graphics::DrawBezier
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
 - Graphics::DrawBezier
---

# DrawBezier(Pen*,REAL,REAL,REAL,REAL,REAL,REAL,REAL,REAL)

## -description

The **Graphics::DrawBezier** method draws a Bézier spline.

## -parameters

### -param pen

Pointer to a pen that is used to draw the Bézier spline.

### -param x1

Real number that specifies the x-coordinate of the starting point of the Bézier spline.

### -param y1

Real number that specifies the y-coordinate of the starting point of the Bézier spline.

### -param x2

Real number that specifies the x-coordinate of the first control point of the Bézier spline.

### -param y2

Real number that specifies the y-coordinate of the first control point of the Bézier spline.

### -param x3

Real number that specifies the x-coordinate of the second control point of the Bézier spline.

### -param y3

Real number that specifies the y-coordinate of the second control point of the Bézier spline.

### -param x4

Real number that specifies the x-coordinate of the ending point of the Bézier spline.

### -param y4

Real number that specifies the y-coordinate of the ending point of the Bézier spline.

## -returns

If the method succeeds, it returns <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Ok</a>, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the **Status** enumeration.

## -remarks

A Bézier spline does not pass through its control points.
The control points act as magnets, pulling the curve in certain directions to influence the way the Bézier spline bends.

#### Examples

The following example draws a Bézier curve.

```cpp
VOID Example_DrawBezier4(HDC hdc)
{
   Graphics graphics(hdc);

   // Set up the pen and curve points.
   Pen greenPen(Color(255, 0, 255, 0));
   REAL startPointx = 100.0f;
   REAL startPointy = 100.0f;
   REAL ctrlPoint1x = 200.0f;
   REAL ctrlPoint1y = 10.0f;
   REAL ctrlPoint2x = 350.0f;
   REAL ctrlPoint2y = 50.0f;
   REAL endPointx = 500.0f;
   REAL endPointy = 100.0f;

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

<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>

<a href="https://msdn.microsoft.com/en-us/library/ms535734(v=VS.85).aspx">DrawBezier</a>

<a href="https://msdn.microsoft.com/en-us/library/ms535738(v=VS.85).aspx">DrawBeziers Methods</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a>

<a href="https://msdn.microsoft.com/en-us/library/ms533926(v=VS.85).aspx">Drawing Bézier Splines</a>

<a href="https://msdn.microsoft.com/en-us/library/ms536354(v=VS.85).aspx">Bézier Splines</a>
