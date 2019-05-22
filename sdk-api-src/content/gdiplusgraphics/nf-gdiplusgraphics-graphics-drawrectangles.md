---
UID: NF:gdiplusgraphics.Graphics.DrawRectangles
title: Graphics::DrawRectangles
description: The Graphics::DrawRectangles method draws a sequence of rectangles.
ms.assetid: d8a6725b-6382-48a4-b83b-0a61614af6c9
ms.author: windowssdkdev
ms.date: 05/13/2019
ms.keywords: Graphics::DrawRectangles
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
 - Graphics::DrawRectangles
---

# DrawRectangles(Pen*,RectF*,INT)

## -description

The **Graphics::DrawRectangles** method draws a sequence of rectangles.

## -parameters

### -param pen

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a> that is used to draw the rectangles.

### -param rects

Pointer to an array of <a href="https://msdn.microsoft.com/en-us/library/ms534497(v=VS.85).aspx">RectF</a> objects that specify the coordinates of the rectangles to be drawn.

### -param count

Integer that specifies the number of elements in the *rects* array.

## -returns

If the method succeeds, it returns <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Ok</a>, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

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

<a href="https://msdn.microsoft.com/en-us/library/ms535757(v=VS.85).aspx">DrawRectangles Methods</a>

<a href="https://msdn.microsoft.com/en-us/library/ms535773(v=VS.85).aspx">FillRectangle Methods</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>

<a href="https://msdn.microsoft.com/en-us/library/ms536372(v=VS.85).aspx">Pens, Lines, and Rectangles</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534495(v=VS.85).aspx">Rect</a>

<a href="https://msdn.microsoft.com/en-us/library/ms533855(v=VS.85).aspx">Using a Pen to Draw Lines and Rectangles</a>