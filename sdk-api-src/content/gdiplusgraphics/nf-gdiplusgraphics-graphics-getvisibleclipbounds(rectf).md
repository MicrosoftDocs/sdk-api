---
UID: NF:gdiplusgraphics.Graphics.GetVisibleClipBounds(RectF)
title: Graphics::GetVisibleClipBounds
description: The Graphics::GetVisibleClipBounds method gets a rectangle that encloses the visible clipping region of this Graphics object. (overload 2/2)
tech.root: gdiplus
helpviewer_keywords: ["Graphics::GetVisibleClipBounds"]
ms.assetid: dda12bab-2ffc-4fca-9280-3bc88798fac2
ms.date: 05/13/2019
ms.keywords: Graphics::GetVisibleClipBounds
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
 - Graphics::GetVisibleClipBounds
 - gdiplusgraphics/Graphics::GetVisibleClipBounds
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdiplusgraphics.h
api_name:
 - Graphics::GetVisibleClipBounds
---

# GetVisibleClipBounds(RectF*)


## -description

The **Graphics::GetVisibleClipBounds** method gets a rectangle that encloses the visible clipping region of this <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object.
The visible clipping region is the intersection of the clipping region of this **Graphics** object and the clipping region of the window.

## -parameters

### -param rect

Pointer to a <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a> object that receives the rectangle that encloses the visible clipping region.

## -returns

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the **Status** enumeration.

## -remarks

#### Examples

The following example sets the clipping region for the **Graphics** object.
It then gets a rectangle that encloses the visible clipping region and fills that rectangle.

```cpp
VOID Example_GetVisibleClipBounds2(HDC hdc)
{
   Graphics graphics(hdc);

   // Set the clipping region.
   graphics.SetClip(RectF(100.0f, 100.0f, 200.0f, 100.0f));

   // Get a bounding rectangle for the clipping region.
   RectF boundRect;
   graphics.GetVisibleClipBounds(&boundRect);

   // Fill the bounding rectangle.
   graphics.FillRectangle(&SolidBrush(Color(255, 0, 0, 0)), boundRect);
}
```

## -see-also

<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-getclipbounds(outrect)">GetClipBounds Methods</a>

<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>

<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-isvisibleclipempty">Graphics::IsVisibleClipEmpty</a>

<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-isvisible(inconstpointf_)">IsVisible Methods</a>

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a>
