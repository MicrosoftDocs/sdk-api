---
UID: NF:gdiplusgraphics.Graphics.DrawRectangle(constPen,constRectF&)
title: Graphics::DrawRectangle
description: The Graphics::DrawRectangle method draws a rectangle. (overload 4/4)
tech.root: gdiplus
helpviewer_keywords: ["Graphics::DrawRectangle"]
ms.assetid: cf3f26ad-2aec-4986-a884-95763e63013e
ms.date: 05/13/2019
ms.keywords: Graphics::DrawRectangle
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
 - Graphics::DrawRectangle
 - gdiplusgraphics/Graphics::DrawRectangle
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdiplusgraphics.h
api_name:
 - Graphics::DrawRectangle
---

# DrawRectangle(Pen*,RectF&)


## -description

The **Graphics::DrawRectangle** method draws a rectangle.

## -parameters

### -param pen

Pointer to a <a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> that is used to draw the rectangle.

### -param rect

Reference to the rectangle to be drawn.

## -returns

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the **Status** enumeration.

## -remarks

#### Examples

The following example draws a rectangle.

```cpp
VOID Example_DrawRectangle2(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a Pen object.
   Pen blackPen(Color(255, 0, 0, 0), 3);

   // Create a RectF object.
   RectF rect(0.0f, 0.0f, 200.0f, 200.0f);

   // Draw rect.
   graphics.DrawRectangle(&blackPen, rect);
}
```

## -see-also

<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangles(inconstpen_inconstrect_inint)">DrawRectangles Methods</a>

<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inconstrect_)">FillRectangle Methods</a>

<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>

<a href="/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a>

<a href="/windows/desktop/gdiplus/-gdiplus-using-a-pen-to-draw-lines-and-rectangles-use">Using a Pen to Draw Lines and Rectangles</a>
