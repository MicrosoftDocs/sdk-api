---
UID: NF:gdiplusgraphics.Graphics.FillPolygon(constBrush,constPointF,INT)
title: Graphics::FillPolygon
description: The Graphics::FillPolygon method uses a brush to fill the interior of a polygon. (overload 3/4)
tech.root: gdiplus
helpviewer_keywords: ["Graphics::FillPolygon"]
ms.assetid: d5922fd8-b17d-4a1f-9e1b-3531f0b7d2d0
ms.date: 05/13/2019
ms.keywords: Graphics::FillPolygon
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
 - Graphics::FillPolygon
 - gdiplusgraphics/Graphics::FillPolygon
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdiplusgraphics.h
api_name:
 - Graphics::FillPolygon
---

# FillPolygon(Brush*,PointF*,INT)


## -description

The **Graphics::FillPolygon** method uses a brush to fill the interior of a polygon.

## -parameters

### -param brush

Pointer to a <a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush">Brush</a> object that is used to paint the interior of the polygon.

### -param points

Pointer to an array of points that make up the vertices of the polygon.
The first two points in the array specify the first side of the polygon.
Each additional point specifies a new side, the vertices of which include the point and the previous point.
If the last point and the first point do not coincide, they specify the last side of the polygon.

### -param count

Integer that specifies the number of points in the *points* array.

## -returns

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the **Status** enumeration.

## -remarks

#### Examples

The following example defines a polygon and then fills it.

```cpp
VOID Example_FillPolygon3(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a SolidBrush object.
   SolidBrush blackBrush(Color(255, 0, 0, 0));

   // Create an array of PointF objects that define the polygon.
   PointF point1(100.0f, 100.0f);
   PointF point2(200.0f, 130.0f);
   PointF point3(150.0f, 200.0f);
   PointF point4(50.0f, 200.0f);
   PointF point5(0.0f, 130.0f);
   PointF points[5] = {point1, point2, point3, point4, point5};

   // Fill the polygon.
   graphics.FillPolygon(&blackBrush, points, 5);
}
```

## -see-also

<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>

<a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a>
