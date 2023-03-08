---
UID: NF:gdiplusgraphics.Graphics.IsVisible(INT,INT)
title: Graphics::IsVisible
description: The Graphics::IsVisible method determines whether the specified point is inside the visible clipping region of this Graphics object. (overload 3/4)
tech.root: gdiplus
helpviewer_keywords: ["Graphics::IsVisible"]
ms.assetid: 81cadd52-1976-4328-85ca-e89aa5b649b5
ms.date: 05/13/2019
ms.keywords: Graphics::IsVisible
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
 - Graphics::IsVisible
 - gdiplusgraphics/Graphics::IsVisible
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdiplusgraphics.h
api_name:
 - Graphics::IsVisible
---

# IsVisible(INT,INT)


## -description

The **Graphics::IsVisible** method determines whether the specified point is inside the visible clipping region of this <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object.
The visible clipping region is the intersection of the clipping region of this **Graphics** object and the clipping region of the window.

## -parameters

### -param x

Integer that specifies the x-coordinate of the point to test.

### -param y

Integer that specifies the y-coordinate of the point to test.

## -returns

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the **Status** enumeration.

## -remarks

#### Examples

The following example tests whether the specified point is visible on the display device.
If it is, it fills an ellipse that represents that point.

```cpp
VOID Example_IsVisible5(HDC hdc)

{
   Graphics graphics(hdc);

   // Set up the coordinates of the point.
   int x = 100;
   int y = 100;

   // If the point (x, y) is visible, fill an ellipse that represents it.
   if (graphics.IsVisible(x, y))
   {
   graphics.FillEllipse(&SolidBrush(Color(255, 0, 0, 0)), x, y, 5, 5);
   }
}
```

## -see-also

<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>

<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-isvisibleclipempty">Graphics::IsVisibleClipEmpty</a>
