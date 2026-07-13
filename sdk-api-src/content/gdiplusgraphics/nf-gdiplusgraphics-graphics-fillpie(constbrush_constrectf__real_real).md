---
UID: NF:gdiplusgraphics.Graphics.FillPie(constBrush,constRectF&,REAL,REAL)
title: Graphics::FillPie
description: The Graphics::FillPie method uses a brush to fill the interior of a pie. (overload 4/4)
tech.root: gdiplus
helpviewer_keywords: ["Graphics::FillPie"]
ms.assetid: b849f776-ca4b-47dc-8442-5f8cc7864677
ms.date: 05/13/2019
ms.keywords: Graphics::FillPie
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
 - Graphics::FillPie
 - gdiplusgraphics/Graphics::FillPie
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdiplusgraphics.h
api_name:
 - Graphics::FillPie
---

# FillPie(Brush*,RectF&,REAL,REAL)


## -description

The **Graphics::FillPie** method uses a brush to fill the interior of a pie.

## -parameters

### -param brush

Pointer to a <a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush">Brush</a> object that is used to paint the interior of the pie.

### -param rect

Reference to a rectangle that bounds the ellipse.
A curved portion of the ellipse is the arc of the pie.

### -param startAngle

Real number that specifies the angle, in degrees, between the x-axis and the starting point of the pie's arc.

### -param sweepAngle

## -returns

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the **Status** enumeration.

## -remarks

A pie is a portion of the interior of an ellipse (it is bounded by an elliptical curve and two radial lines).
The *startAngle* and *sweepAngle* specify the portion of the ellipse to be used.

#### Examples

The following example defines a pie and then fills it.

```cpp
VOID Example_FillPie2(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a SolidBrush object.
   SolidBrush blackBrush(Color(255, 0, 0, 0));

   // Define the pie shape.
   RectF ellipseRect(0.5f, 0.8f, 200.9f, 100.6f);
   REAL startAngle = 0.0;
   REAL sweepAngle = 45.8;

   // Fill the pie.
   graphics.FillPie(&blackBrush, ellipseRect, startAngle, sweepAngle);
}
```

## -see-also

<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>

<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>

<a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a>
