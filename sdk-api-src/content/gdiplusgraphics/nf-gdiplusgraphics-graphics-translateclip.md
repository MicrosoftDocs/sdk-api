---
UID: NF:gdiplusgraphics.Graphics.TranslateClip
title: Graphics::TranslateClip
description: The Graphics::TranslateClip method translates the clipping region of this Graphics object.
ms.assetid: 323bc752-60d5-44f5-88dd-6bf0c4c0c926
ms.author: windowssdkdev
ms.date: 05/13/2019
ms.keywords: Graphics::TranslateClip
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
 - Graphics::TranslateClip
---

# TranslateClip(REAL,REAL)

## -description

The **Graphics::TranslateClip** method translates the clipping region of this <a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object.

## -parameters

### -param dx

Real number that specifies the horizontal component of the translation.

### -param dy

Real number that specifies the vertical component of the translation.

## -returns

If the method succeeds, it returns <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Ok</a>, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

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

<a href="https://msdn.microsoft.com/en-us/library/ms536360(v=VS.85).aspx">Clipping</a>

<a href="https://msdn.microsoft.com/en-us/library/ms533825(v=VS.85).aspx">Clipping with a Region</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>

<a href="https://msdn.microsoft.com/en-us/library/ms535698(v=VS.85).aspx">Graphics::GetClip</a>

<a href="https://msdn.microsoft.com/en-us/library/ms535792(v=VS.85).aspx">Graphics::IsClipEmpty</a>

<a href="https://msdn.microsoft.com/en-us/library/ms535783(v=VS.85).aspx">IntersectClip Methods</a>

<a href="https://msdn.microsoft.com/en-us/library/ms535789(v=VS.85).aspx">SetClip Methods</a>
