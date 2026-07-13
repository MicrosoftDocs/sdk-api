---
UID: NF:gdiplusheaders.Region.GetBounds(Rect,constGraphics)
title: Region::GetBounds
description: The Region::GetBounds method gets a rectangle that encloses this region. (overload 2/2)
tech.root: gdiplus
helpviewer_keywords: ["Region::GetBounds"]
ms.assetid: fdbecca4-be04-4162-a930-19e94c69c7e2
ms.date: 05/20/2019
ms.keywords: Region::GetBounds
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: gdiplusheaders.h
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
 - Region::GetBounds
 - gdiplusheaders/Region::GetBounds
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdiplusheaders.h
api_name:
 - Region::GetBounds
---

# Region::GetBounds(Rect*,Graphics*)


## -description

The **Region::GetBounds** method gets a rectangle that encloses this region.

## -parameters

### -param rect

Pointer to a <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a> object that receives the enclosing rectangle.

### -param g

Pointer to a <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object that contains the world and page transformations required to calculate the device coordinates of this region and the rectangle.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

The current world and page transformations of the graphics object are used to calculate the region and the rectangle as they are drawn on the display device.
The rectangle returned by **Region::GetBounds** is not always the smallest possible rectangle.

#### Examples

The following example creates a region from a path, gets the region's enclosing rectangle, and then displays both.

```cpp
VOID Example_GetBoundsRect(HDC hdc)
{
   Graphics graphics(hdc);

   Point points[] = {
      Point(110, 20),
      Point(120, 30),
      Point(100, 60),
      Point(120, 70),
      Point(150, 60),
      Point(140, 10)};

   GraphicsPath path;
    SolidBrush solidBrush(Color(255, 255, 0, 0));
    Pen pen(Color(255, 0, 0, 0));
    Rect rect;

   path.AddClosedCurve(points, 6);

    // Create a region from a path.
    Region pathRegion(&path);

    // Get the region's enclosing rectangle.
    pathRegion.GetBounds(&rect, &graphics);

    // Show the region and the enclosing rectangle.
    graphics.FillRegion(&solidBrush, &pathRegion);
    graphics.DrawRectangle(&pen, rect);
}
```

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a>

<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>

<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>
