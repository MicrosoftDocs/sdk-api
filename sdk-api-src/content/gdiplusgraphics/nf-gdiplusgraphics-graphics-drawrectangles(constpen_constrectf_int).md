---
UID: NF:gdiplusgraphics.Graphics.DrawRectangles(constPen,constRectF,INT)
title: Graphics::DrawRectangles
description: The Graphics::DrawRectangles method draws a sequence of rectangles. (overload 2/2)
tech.root: gdiplus
helpviewer_keywords: ["Graphics::DrawRectangles"]
ms.assetid: d8a6725b-6382-48a4-b83b-0a61614af6c9
ms.date: 05/13/2019
ms.keywords: Graphics::DrawRectangles
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
 - Graphics::DrawRectangles
 - gdiplusgraphics/Graphics::DrawRectangles
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdiplusgraphics.h
api_name:
 - Graphics::DrawRectangles
---

# DrawRectangles(Pen*,RectF*,INT)


## -description

The **Graphics::DrawRectangles** method draws a sequence of rectangles.

## -parameters

### -param pen

Pointer to a <a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> that is used to draw the rectangles.

### -param rects

Pointer to an array of <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a> objects that specify the coordinates of the rectangles to be drawn.

### -param count

Integer that specifies the number of elements in the *rects* array.

## -returns

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the **Status** enumeration.

## -remarks

#### Examples

The following example draws a group of rectangles.

```cpp
VOID Example_DrawRectangles2(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a Pen object.
   Pen blackPen(Color(255, 0, 0, 0), 3);
   
   // Create an array of RectF objects.
   RectF rect1(0.0f, 0.0f, 100.0f, 200.0f);
   RectF rect2(100.0f, 200.0f, 250.0f, 50.0f);
   RectF rect3(300.0f, 0.0f, 50.0f, 100.0f);
   RectF rects[] = {rect1, rect2, rect3};
   RectF* pRects = rects;

   // Draw the rectangles.
   graphics.DrawRectangles(&blackPen, pRects, 3);
}
```

## -see-also

<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangles(inconstpen_inconstrect_inint)">DrawRectangles Methods</a>

<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inconstrect_)">FillRectangle Methods</a>

<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>

<a href="/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>

<a href="/windows/desktop/gdiplus/-gdiplus-using-a-pen-to-draw-lines-and-rectangles-use">Using a Pen to Draw Lines and Rectangles</a>
