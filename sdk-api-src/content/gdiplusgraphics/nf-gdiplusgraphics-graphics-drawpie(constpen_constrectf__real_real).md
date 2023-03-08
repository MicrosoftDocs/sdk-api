---
UID: NF:gdiplusgraphics.Graphics.DrawPie(constPen,constRectF&,REAL,REAL)
title: Graphics::DrawPie
description: The Graphics::DrawPie method draws a pie. (overload 1/4)
tech.root: gdiplus
helpviewer_keywords: ["Graphics::DrawPie"]
ms.assetid: 603dcdca-09bb-4a1a-a04a-6a47be08bfc0
ms.date: 05/13/2019
ms.keywords: Graphics::DrawPie
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
 - Graphics::DrawPie
 - gdiplusgraphics/Graphics::DrawPie
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdiplusgraphics.h
api_name:
 - Graphics::DrawPie
---

# DrawPie(Pen*,RectF&,REAL,REAL)


## -description

The **Graphics::DrawPie** method draws a pie.

## -parameters

### -param pen

Pointer to a pen that is used to draw the pie.

### -param rect

Rectangle that bounds the ellipse in which to draw the pie.

### -param startAngle

Real number that specifies the angle, in degrees, between the x-axis and the starting point of the arc that defines the pie.
A positive value specifies clockwise rotation.

### -param sweepAngle

Real number that specifies the angle, in degrees, between the starting and ending points of the arc that defines the pie.
A positive value specifies clockwise rotation.

## -returns

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the **Status** enumeration.

## -remarks

#### Examples

The following example draws a pie.

```cpp
VOID Example_DrawPie2(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a Pen object.
   Pen blackPen(Color(255, 0, 0, 0), 3);

   // Define the pie.
   RectF ellipseRect(0, 0, 200, 100);
   REAL startAngle = 0.0f;
   REAL sweepAngle = 45.0f;

   // Draw the pie.
   graphics.DrawPie(&blackPen, ellipseRect, startAngle, sweepAngle);
}
```

## -see-also

<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inconstrect__inreal_inreal)">FillPie Methods</a>

<a href="/windows/desktop/gdiplus/-gdiplus-open-and-closed-curves-about">Open and Closed Curves</a>

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a>
