---
UID: NF:gdiplusgraphics.Graphics.FillRectangle(constBrush,constRectF&)
title: Graphics::FillRectangle
description: The Graphics::FillRectangle method uses a brush to fill the interior of a rectangle. (overload 1/4)
tech.root: gdiplus
helpviewer_keywords: ["Graphics::FillRectangle"]
ms.assetid: 8e8ec281-ff99-4fc7-bbf0-77d1ca3f128e
ms.date: 05/13/2019
ms.keywords: Graphics::FillRectangle
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
 - Graphics::FillRectangle
 - gdiplusgraphics/Graphics::FillRectangle
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdiplusgraphics.h
api_name:
 - Graphics::FillRectangle
---

# FillRectangle(Brush*,RectF&)


## -description

The **Graphics::FillRectangle** method uses a brush to fill the interior of a rectangle.

## -parameters

### -param brush

Pointer to a <a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush">Brush</a> that is used to paint the interior of the rectangle.

### -param rect

Reference to the rectangle to be filled.

## -returns

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the **Status** enumeration.

## -remarks

#### Examples

```cpp
VOID Example_FillRectangle2(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a SolidBrush object.
   SolidBrush blackBrush(Color(255, 0, 0, 0));

   // Create a RectF object.
   RectF fillRect(1.0f, 2.5f, 100.3f, 100.9f);

   // Fill the rectangle.
   graphics.FillRectangle(&blackBrush, fillRect);
}
```

## -see-also

<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>

<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>

<a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a>
