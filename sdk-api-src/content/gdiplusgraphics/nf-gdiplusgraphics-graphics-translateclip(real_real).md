---
UID: NF:gdiplusgraphics.Graphics.TranslateClip(REAL,REAL)
title: Graphics::TranslateClip
description: The Graphics::TranslateClip method translates the clipping region of this Graphics object. (overload 1/2)
tech.root: gdiplus
helpviewer_keywords: ["Graphics::TranslateClip"]
ms.assetid: 323bc752-60d5-44f5-88dd-6bf0c4c0c926
ms.date: 05/13/2019
ms.keywords: Graphics::TranslateClip
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
 - Graphics::TranslateClip
 - gdiplusgraphics/Graphics::TranslateClip
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdiplusgraphics.h
api_name:
 - Graphics::TranslateClip
---

# TranslateClip(REAL,REAL)


## -description

The **Graphics::TranslateClip** method translates the clipping region of this <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object.

## -parameters

### -param dx

Real number that specifies the horizontal component of the translation.

### -param dy

Real number that specifies the vertical component of the translation.

## -returns

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the **Status** enumeration.

## -remarks

#### Examples

The following example measures the size of a string and then draws a rectangle that represents that size.

```cpp
VOID Example_TranslateClipReal(HDC hdc)
{
   Graphics graphics(hdc);

   // Set the clipping region.
   graphics.SetClip(RectF(0.0f, 0.0f, 100.0f, 50.0f));

   // Translate the clipping region.
   graphics.TranslateClip(40.0f, 30.0f);

   // Fill an ellipse that is clipped by the translated clipping region.
   SolidBrush brush(Color(255, 255, 0, 0));
   graphics.FillEllipse(&brush, 20, 40, 100, 80);

   // Draw the outline of the clipping region (rectangle).
   Pen pen(Color(255, 0, 0, 0), 2.0f);
   graphics.DrawRectangle(&pen, 40, 30, 100, 50);
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-clipping-about">Clipping</a>

<a href="/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>

<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>

<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-getclip">Graphics::GetClip</a>

<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-isclipempty">Graphics::IsClipEmpty</a>

<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-intersectclip(inconstrect_)">IntersectClip Methods</a>

<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstgraphicspath_incombinemode)">SetClip Methods</a>
