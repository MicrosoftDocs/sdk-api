---
UID: NF:gdiplusgraphics.Graphics.DrawLine(constPen,REAL,REAL,REAL,REAL)
title: Graphics::DrawLine
description: The Graphics::DrawLine method draws a line that connects two points. (overload 1/4)
tech.root: gdiplus
helpviewer_keywords: ["Graphics::DrawLine"]
ms.assetid: b245ba2b-4b52-40fa-b6f3-adcd25775b94
ms.date: 05/13/2019
ms.keywords: Graphics::DrawLine
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
 - Graphics::DrawLine
 - gdiplusgraphics/Graphics::DrawLine
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdiplusgraphics.h
api_name:
 - Graphics::DrawLine
---

# DrawLine(Pen*,REAL,REAL,REAL,REAL)


## -description

The **Graphics::DrawLine** method draws a line that connects two points.

## -parameters

### -param pen

Pointer to a pen that is used to draw the line.

### -param x1

Real number that specifies the x-coordinate of the starting point of the line.

### -param y1

Real number that specifies the y-coordinate of the starting point of the line.

### -param x2

Real number that specifies the x-coordinate of the ending point of the line.

### -param y2

Real number that specifies the y-coordinate of the ending point of the line.

## -returns

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the **Status** enumeration.

## -remarks

#### Examples

The following example draws a line.

```cpp
VOID Example_DrawLine4(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a Pen object.
   Pen blackPen(Color(255, 0, 0, 0), 3);

   // Initialize the coordinates of the points that define the line.
   REAL x1 = 100.0f;
   REAL y1 = 100.0f;
   REAL x2 = 500.0f;
   REAL y2 = 100.0f;

   // Draw the line.
   graphics.DrawLine(&blackPen, x1, y1, x2, y2);
}
```

## -see-also

<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawlines(inconstpen_inconstpoint_inint)">DrawLines Methods</a>

<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>

<a href="/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a>

<a href="/windows/desktop/gdiplus/-gdiplus-using-a-pen-to-draw-lines-and-rectangles-use">Using a Pen to Draw Lines and Rectangles</a>
