---
UID: NF:gdiplusgraphics.Graphics.FillClosedCurve
title: Graphics::FillClosedCurve
description: The Graphics::FillClosedCurve method creates a closed cardinal spline from an array of points and uses a brush to fill the interior of the spline.
ms.assetid: 2aea6910-6fd0-4611-9de6-65ee0b65421e
ms.author: windowssdkdev
ms.date: 05/13/2019
ms.keywords: Graphics::FillClosedCurve
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
 - Graphics::FillClosedCurve
---

# FillClosedCurve(Brush*,PointF*,INT)

## -description

The **Graphics::FillClosedCurve** method creates a closed cardinal spline from an array of points and uses a brush to fill the interior of the spline.

## -parameters

### -param brush

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534424(v=VS.85).aspx">Brush</a> object that is used to paint the interior of the spline.

### -param points

Pointer to an array of points that this method uses to create a closed cardinal spline. Each point in the array is a point on the spline.

### -param count

Integer that specifies the number of points in the *points* array.

## -returns

If the method succeeds, it returns <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Ok</a>, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the **Status** enumeration.

## -remarks

#### Examples

The following example fills a closed cardinal spline.

```cpp
VOID Example_FillClosedCurve3(HDC hdc)
{
   Graphics graphics(hdc);

   //Create a SolidBrush object.
   SolidBrush blackBrush(Color(255, 0, 0, 0));

   //Create an array of PointF objects.
   PointF point1(100.0f, 100.0f);
   PointF point2(200.0f, 50.0f);
   PointF point3(250.0f, 200.0f);
   PointF point4(50.0f, 150.0f);
   PointF points[4] = {point1, point2, point3, point4};

   //Fill the curve.
   graphics.FillClosedCurve(&blackBrush, points, 4);
}
```

## -see-also

<a href="https://msdn.microsoft.com/en-us/library/ms536358(v=VS.85).aspx">Cardinal Splines</a>

<a href="https://msdn.microsoft.com/en-us/library/ms533934(v=VS.85).aspx">Drawing Cardinal Splines</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>

<a href="https://msdn.microsoft.com/en-us/library/ms536366(v=VS.85).aspx">Open and Closed Curves</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534487(v=VS.85).aspx">Point</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534508(v=VS.85).aspx">SolidBrush</a>

<a href="https://msdn.microsoft.com/en-us/library/ms536356(v=VS.85).aspx">Brushes and Filled Shapes</a>
