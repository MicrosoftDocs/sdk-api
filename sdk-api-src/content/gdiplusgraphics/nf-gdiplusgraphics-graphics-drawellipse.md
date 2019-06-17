---
UID: NF:gdiplusgraphics.Graphics.DrawEllipse
title: Graphics::DrawEllipse
description: The Graphics::DrawEllipse method draws an ellipse.
ms.assetid: c520987b-a425-4959-b293-5988de01a553
ms.author: windowssdkdev
ms.date: 05/13/2019
ms.keywords: Graphics::DrawEllipse
ms.topic: language-reference
f1_keywords: ["gdiplusgraphics/Graphics::DrawEllipse"]
targetos: Windows
product: Windows
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
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdiplusgraphics.h
api_name:
 - Graphics::DrawEllipse
---

# DrawEllipse(Pen*,RectF&)

## -description

The **Graphics::DrawEllipse** method draws an ellipse.

## -parameters

### -param pen

Pointer to a pen that is used to draw the ellipse.

### -param rect

Reference to a rectangle that bounds the ellipse.

## -returns

If the method succeeds, it returns <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the **Status** enumeration.

## -remarks

#### Examples

The following example draws an ellipse.

```cpp
VOID Example_DrawEllipse2(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a Pen object.
   Pen bluePen(Color(255, 0, 0, 255));

   // Create a Rect object that bounds the ellipse.
   RectF ellipseRect(0.0f, 0.0f, 200.0f, 100.0f);

   // Draw the ellipse.
   graphics.DrawEllipse(&bluePen, ellipseRect);
}
```

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>

<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inconstrect_)">FillEllipse Methods</a>

<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>

<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a>

<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-ellipses-and-arcs-about">Ellipses and Arcs</a>
