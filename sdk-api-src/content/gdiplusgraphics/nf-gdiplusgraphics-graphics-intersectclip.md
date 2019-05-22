---
UID: NF:gdiplusgraphics.Graphics.IntersectClip
title: Graphics::IntersectClip
description: The Graphics::IntersectClip method updates the clipping region of this Graphics object.
ms.assetid: 9aa49ff6-adce-4495-9af2-719ad029f751
ms.author: windowssdkdev
ms.date: 05/13/2019
ms.keywords: Graphics::IntersectClip
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
 - Graphics::IntersectClip
---

# IntersectClip(RectF&)

## -description

The **Graphics::IntersectClip** method updates the clipping region of this <a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object to the portion of the specified rectangle that intersects with the current clipping region of this **Graphics** object.

## -parameters

### -param rect

Reference to a rectangle that is used to update the clipping region.

## -returns

If the method succeeds, it returns <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Ok</a>, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the **Status** enumeration.

## -remarks

#### Examples

The following example sets a clipping region and updates the clipping region.
It then draws rectangles to demonstrate the effective clipping region.

```cpp
VOID Example_IntersectClip2(HDC hdc)
{
   Graphics graphics(hdc);

   // Set the clipping region.
   RectF clipRect(0.5f, 0.5f, 200.5f, 200.5f);
   graphics.SetClip(clipRect);

   // Update the clipping region to the portion of the rectangle that
   // intersects with the current clipping region.
   RectF intersectRect(100.5f, 100.5f, 200.5f, 200.5f);
   graphics.IntersectClip(intersectRect);

   // Fill a rectangle to demonstrate the effective clipping region.
   graphics.FillRectangle(&SolidBrush(Color(255, 0, 0, 255)), 0, 0, 500, 500);

   // Reset the clipping region to infinite.
   graphics.ResetClip();

   // Draw clipRect and intersectRect.
   graphics.DrawRectangle(&Pen(Color(255, 0, 0, 0)), clipRect);
   graphics.DrawRectangle(&Pen(Color(255, 255, 0, 0)), intersectRect);
}
```

## -see-also

<a href="https://msdn.microsoft.com/en-us/library/ms536360(v=VS.85).aspx">Clipping</a>

<a href="https://msdn.microsoft.com/en-us/library/ms533825(v=VS.85).aspx">Clipping with a Region</a>

<a href="https://msdn.microsoft.com/en-us/library/ms535780(v=VS.85).aspx">GetClipBounds Methods</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>

<a href="https://msdn.microsoft.com/en-us/library/ms535698(v=VS.85).aspx">Graphics::GetClip</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534497(v=VS.85).aspx">RectF</a>

<a href="https://msdn.microsoft.com/en-us/library/ms535789(v=VS.85).aspx">SetClip Methods</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a>
