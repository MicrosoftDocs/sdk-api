---
UID: NF:gdiplusgraphics.Graphics.DrawRectangle
title: Graphics::DrawRectangle
description: The Graphics::DrawRectangle method draws a rectangle.
ms.assetid: cf3f26ad-2aec-4986-a884-95763e63013e
ms.author: windowssdkdev
ms.date: 05/13/2019
ms.keywords: Graphics::DrawRectangle
ms.topic: language-reference
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
 - Graphics::DrawRectangle
---

# DrawRectangle(Pen*,RectF&)

## -description

The **Graphics::DrawRectangle** method draws a rectangle.

## -parameters

### -param pen

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a> that is used to draw the rectangle.

### -param rect

Reference to the rectangle to be drawn.

## -returns

If the method succeeds, it returns <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Ok</a>, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

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

<a href="https://msdn.microsoft.com/en-us/library/ms535757(v=VS.85).aspx">DrawRectangles Methods</a>

<a href="https://msdn.microsoft.com/en-us/library/ms535773(v=VS.85).aspx">FillRectangle Methods</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>

<a href="https://msdn.microsoft.com/en-us/library/ms536372(v=VS.85).aspx">Pens, Lines, and Rectangles</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534497(v=VS.85).aspx">RectF</a>

<a href="https://msdn.microsoft.com/en-us/library/ms533855(v=VS.85).aspx">Using a Pen to Draw Lines and Rectangles</a>
