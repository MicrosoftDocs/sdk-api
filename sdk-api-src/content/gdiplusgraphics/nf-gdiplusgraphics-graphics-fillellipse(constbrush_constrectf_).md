---
UID: NF:gdiplusgraphics.Graphics.FillEllipse(constBrush,constRectF&)
title: Graphics::FillEllipse
description: The **Graphics::FillEllipse** method uses a brush to fill the interior of an ellipse that is specified by a rectangle.
tech.root: gdiplus
helpviewer_keywords: ["Graphics::FillEllipse"]
ms.assetid: a89598db-a1b9-404a-a2bc-1a0a94afb8d4
ms.date: 05/13/2019
ms.keywords: Graphics::FillEllipse
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
 - Graphics::FillEllipse
 - gdiplusgraphics/Graphics::FillEllipse
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdiplusgraphics.h
api_name:
 - Graphics::FillEllipse
---

# FillEllipse(Brush*,RectF&)


## -description

The **Graphics::FillEllipse** method uses a brush to fill the interior of an ellipse that is specified by a rectangle.

## -parameters

### -param brush

Pointer to a <a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush">Brush</a> object that is used to paint the interior of the ellipse.

### -param rect

Reference to a rectangle that specifies the boundaries of the ellipse.

## -returns

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the **Status** enumeration.

## -remarks

#### Examples

The following example fills an ellipse defined by a bounding rectangle.

```cpp
VOID Example_FillEllipse2(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a SolidBrush object.
   SolidBrush blackBrush(Color(255, 0, 0, 0));

   // Create the RectF object that defines the ellipse.
   RectF ellipseRect(0.0f, 0.6f, 200.8f, 100.9f);

   // Fill the ellipse.
   graphics.FillEllipse(&blackBrush, ellipseRect);
}
```

## -see-also

<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush">Brush</a>

<a href="/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>

<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a>

<a href="/windows/desktop/gdiplus/-gdiplus-using-a-brush-to-fill-shapes-use">Using a Brush to Fill Shapes</a>