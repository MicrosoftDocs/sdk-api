---
UID: NF:gdiplusgraphics.Graphics.GetClipBounds(RectF)
title: Graphics::GetClipBounds
description: The Graphics::GetClipBounds method gets a rectangle that encloses the clipping region of this Graphics object. (overload 2/2)
tech.root: gdiplus
helpviewer_keywords: ["Graphics::GetClipBounds"]
ms.assetid: e33964c8-d643-420c-87d7-91fc561bcd1d
ms.date: 05/13/2019
ms.keywords: Graphics::GetClipBounds
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
 - Graphics::GetClipBounds
 - gdiplusgraphics/Graphics::GetClipBounds
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdiplusgraphics.h
api_name:
 - Graphics::GetClipBounds
---

# GetClipBounds(RectF*)


## -description

The **Graphics::GetClipBounds** method gets a rectangle that encloses the clipping region of this <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object.

## -parameters

### -param rect

Pointer to a <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a> object that receives the rectangle that encloses the clipping region.

## -returns

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the **Status** enumeration.

## -remarks

The world transformation is applied to the clipping region and then the enclosing rectangle is calculated.

If you do not explicitly set the clipping region of a **Graphics** object, its clipping region is infinite.
When the clipping region is infinite, **Graphics::GetClipBounds** returns a large rectangle.
The X and Y data members of that rectangle are large negative numbers, and the *Width* and *Height* data members are large positive numbers.


#### Examples

The following example sets a clipping region, gets the rectangle that encloses the clipping region, and then fills the rectangle.

```cpp
VOID Example_GetClipBounds2(HDC hdc)
{
   Graphics graphics(hdc);

   Region   myRegion(RectF(25.0f, 25.0f, 100.0f, 50.0f));
   RectF    rect(40.0f, 60.0f, 100.0f, 50.0f);
   Region   gRegion;
   RectF    enclosingRect;

   SolidBrush  blueBrush(Color(100, 0, 0, 255));
   Pen         greenPen(Color(255, 0, 255, 0), 1.5f);

   // Modify the region by using a rectangle.
   myRegion.Union(rect);

   // Set the clipping region of the graphics object.
   graphics.SetClip(&myRegion);

   // Now, get the clipping region, and fill it
   graphics.GetClip(&gRegion);
   graphics.FillRegion(&blueBrush, &gRegion);

   // Get a rectangle that encloses the clipping region, and draw the enclosing
   // rectangle.
   graphics.GetClipBounds(&enclosingRect);
   graphics.ResetClip();
   graphics.DrawRectangle(&greenPen, enclosingRect);}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-clipping-about">Clipping</a>

<a href="/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>

<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-getvisibleclipbounds(outrect)">GetVisibleClipBounds Methods</a>

<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>

<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-getclip">Graphics::GetClip</a>

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a>

<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstgraphicspath_incombinemode)">SetClip Methods</a>

<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>
