---
UID: NF:gdiplusgraphics.Graphics.DrawArc(constPen,REAL,REAL,REAL,REAL,REAL,REAL)
title: Graphics::DrawArc
description: The Graphics::DrawArc method draws an arc.
tech.root: gdiplus
helpviewer_keywords: ["Graphics::DrawArc"]
ms.assetid: b4936938-7337-43d8-8cc1-ff1f6d3f6b24
ms.date: 05/13/2019
ms.keywords: Graphics::DrawArc
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
 - Graphics::DrawArc
 - gdiplusgraphics/Graphics::DrawArc
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdiplusgraphics.h
api_name:
 - Graphics::DrawArc
---

# DrawArc(Pen*,REAL,REAL,REAL,REAL,REAL,REAL)


## -description

The **Graphics::DrawArc** method draws an arc.
The arc is part of an ellipse.

## -parameters

### -param pen

Pointer to a pen that is used to draw the arc.

### -param x

Real number that specifies the x-coordinate of the upper-left corner of the bounding rectangle for the ellipse that contains the arc.

### -param y

Real number that specifies the y-coordinate of the upper-left corner of the bounding rectangle for the ellipse that contains the arc.

### -param width

Real number that specifies the width of the ellipse that contains the arc.

### -param height

Real number that specifies the height of the ellipse that contains the arc.

### -param startAngle

Real number that specifies the angle between the x-axis and the starting point of the arc.

### -param sweepAngle

Real number that specifies the angle between the starting and ending points of the arc.

## -returns

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the **Status** enumeration.

## -remarks

#### Examples

The following example draws a 90-degree arc.

```cpp
VOID Example_DrawArc4(HDC hdc)
{
   Graphics graphics(hdc);

   // Set up the arc.
   Pen redPen(Color(255, 255, 0, 0), 3);
   REAL x = 0;
   REAL y = 0;
   REAL width = 200.0f;
   REAL height = 100.0f;
   REAL startAngle = 0.0f;
   REAL sweepAngle = 90.0f;

   // Draw the arc.
   graphics.DrawArc(&redPen, x, y, width, height, startAngle, sweepAngle);
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-creating-figures-from-lines-curves-and-shapes-use">Creating Figures from Lines, Curves, and Shapes</a>

<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inconstrectf__inreal_inreal)">DrawArc Methods</a>

<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)">DrawEllipse Methods</a>

<a href="/windows/desktop/gdiplus/-gdiplus-ellipses-and-arcs-about">Ellipses and Arcs</a>

<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>

<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>