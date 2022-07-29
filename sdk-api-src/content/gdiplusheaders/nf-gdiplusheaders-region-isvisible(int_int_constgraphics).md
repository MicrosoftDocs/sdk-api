---
UID: NF:gdiplusheaders.Region.IsVisible(INT,INT,constGraphics)
title: Region::IsVisible
description: The Region::IsVisible method determines whether a point is inside this region. (overload 2/4)
tech.root: gdiplus
helpviewer_keywords: ["Region::IsVisible"]
ms.assetid: 6e7059c0-2029-4178-961a-88738894ee83
ms.date: 05/20/2019
ms.keywords: Region::IsVisible
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
 - Region::IsVisible
 - gdiplusheaders/Region::IsVisible
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdiplusheaders.h
api_name:
 - Region::IsVisible
---

# Region::IsVisible(INT,INT,Graphics*)


## -description

The **Region::IsVisible** method determines whether a point is inside this region.

## -parameters

### -param x

Integer that specifies the x-coordinate of the point to test.

### -param y

Integer that specifies the y-coordinate of the point to test.

### -param g

Optional.
Pointer to a <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object that contains the world and page transformations required to calculate the device coordinates of this region and the point.
The default value is **NULL**.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

#### Examples

The following example creates a region from a path and then tests to determine whether a point is inside the region.

```cpp
VOID Example_IsVisibleXY(HDC hdc)
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

   path.AddClosedCurve(points, 6);

   // Create a region from a path.
   Region pathRegion(&path);
   graphics.FillRegion(&solidBrush, &pathRegion);

   // Check to see whether the point (125, 40) is in the region.
   INT x = 125;
   INT y = 40;
   if(pathRegion.IsVisible(x, y, &graphics))
   {

      // The point is in the region.
   }

   // Fill a small circle centered at the point (125, 40).
   SolidBrush brush(Color(255, 0, 0, 0));
   graphics.FillEllipse(&brush, x - 4, y - 4, 8, 8);
}
```

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a>

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>

<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>
