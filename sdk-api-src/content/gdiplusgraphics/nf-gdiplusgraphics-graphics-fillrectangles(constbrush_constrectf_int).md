---
UID: NF:gdiplusgraphics.Graphics.FillRectangles(constBrush,constRectF,INT)
title: Graphics::FillRectangles
description: The Graphics::FillRectangles method uses a brush to fill the interior of a sequence of rectangles. (overload 1/2)
tech.root: gdiplus
helpviewer_keywords: ["Graphics::FillRectangles"]
ms.assetid: 6624bdf9-20c4-42f3-a52e-62455ee1e573
ms.date: 05/13/2019
ms.keywords: Graphics::FillRectangles
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
 - Graphics::FillRectangles
 - gdiplusgraphics/Graphics::FillRectangles
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdiplusgraphics.h
api_name:
 - Graphics::FillRectangles
---

# FillRectangles(Brush*,RectF*,INT)


## -description

The **Graphics::FillRectangles** method uses a brush to fill the interior of a sequence of rectangles.

## -parameters

### -param brush

Pointer to a <a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush">Brush</a> that is used to fill the interior of each rectangle.

### -param rects

Pointer to an array of rectangles to be filled.

### -param count

Integer that specifies the number of rectangles in the *rects* array.

## -returns

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the **Status** enumeration.

## -remarks

#### Examples

The following example fills a sequence of rectangles.

```cpp
VOID Example_FillRectangles2(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a SolidBrush object.
   SolidBrush blackBrush(Color(255, 0, 0, 0));

   // Create an array of RectF objects.
   RectF rect1(0.0f, 0.0f, 100.0f, 200.0f);
   RectF rect2(100.5f, 200.5f, 200.5f, 50.5f);
   RectF rect3(300.8f, 0.8f, 50.8f, 150.8f);
   RectF rects[3] = {rect1, rect2, rect3};

   // Fill the rectangles.
   graphics.FillRectangles(&blackBrush, rects, 3);
}
```

## -see-also

<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>

<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>

<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>
