---
UID: NF:gdiplusgraphics.Graphics.ExcludeClip
title: Graphics::ExcludeClip
description: The Graphics::ExcludeClip method updates the clipping region to the portion of itself that does not intersect the specified rectangle.
ms.assetid: 3123dbf3-ea4c-4597-abe8-7fb97ec669f5
ms.author: windowssdkdev
ms.date: 05/13/2019
ms.keywords: Graphics::ExcludeClip
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
 - Graphics::ExcludeClip
---

# ExcludeClip(RectF&)

## -description

The **Graphics::ExcludeClip** method updates the clipping region to the portion of itself that does not intersect the specified rectangle.

## -parameters

### -param rect

Reference to a rectangle to use to update the clipping region.

## -returns

If the method succeeds, it returns <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Ok</a>, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the **Status** enumeration.

## -remarks

#### Examples

The following example uses a rectangle to update a clipping region and then draws a rectangle that demonstrates the updated clipping region.

```cpp
VOID Example_ExcludeClip2(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a RectF object, and set the clipping region to its exclusion.
   RectF excludeRect(100.0f, 100.0f, 200.0f, 200.0f);
   graphics.ExcludeClip(excludeRect);

   // Fill a rectangle to demonstrate the clipping region.
   graphics.FillRectangle(&SolidBrush((255, 0, 0, 255)), 0, 0, 600, 600);
}
```

## -see-also

<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534495(v=VS.85).aspx">Rect</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534510(v=VS.85).aspx">StringFormat</a>