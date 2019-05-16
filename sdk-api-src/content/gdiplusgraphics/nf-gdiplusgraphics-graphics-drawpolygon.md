---
UID: NF:gdiplusgraphics.Graphics.DrawPolygon
title: Graphics::DrawPolygon
description: The Graphics::DrawPolygon method draws a polygon.
ms.assetid: b9ae10d3-96a9-47eb-9a66-f8a118c4e2ef
ms.author: windowssdkdev
ms.date: 05/13/2019
ms.keywords: Graphics::DrawPolygon
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
 - Graphics::DrawPolygon
---

# DrawPolygon(Pen*,PointF*,INT*)

## -description

The **Graphics::DrawPolygon** method draws a polygon.

## -parameters

### -param pen

Pointer to a pen that is used to draw the polygon.

### -param points

Pointer to an array of <a href="https://msdn.microsoft.com/en-us/library/ms534488(v=VS.85).aspx">PointF</a> objects that specify the vertices of the polygon.

### -param count

Integer that specifies the number of elements in the *points* array.

## -returns

If the method succeeds, it returns <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Ok</a>, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the **Status** enumeration.

## -remarks

If the first and last coordinates in the *points* array are not identical, a line is drawn between them to close the polygon.

#### Examples

The following example draws a polygon, defined by an array of points.

```cpp
VOID Example_DrawPolygon2(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a Pen object.
   Pen blackPen(Color(255, 0, 0, 0), 3);

   // Create an array of PointF objects that define the polygon.
   PointF point1(100.0f, 100.0f);
   PointF point2(200.0f, 130.0f);
   PointF point3(150.0f, 200.0f);
   PointF point4(50.0f, 200.0f);
   PointF point5(0.0f, 130.0f);
   PointF points[5] = {point1, point2, point3, point4, point5};
   PointF* pPoints = points;

   // Draw the polygon.
   graphics.DrawPolygon(&blackPen, pPoints, 5);
}
```

## -see-also

<a href="https://msdn.microsoft.com/en-us/library/ms535770(v=VS.85).aspx">FillPolygon Methods</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534488(v=VS.85).aspx">PointF</a>

<a href="https://msdn.microsoft.com/en-us/library/ms536374(v=VS.85).aspx">Polygons</a>
