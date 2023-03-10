---
UID: NF:gdiplusheaders.Region.Translate(REAL,REAL)
title: Region::Translate
description: The Region::Translate method offsets this region by specified amounts in the horizontal and vertical directions. (overload 2/2)
tech.root: gdiplus
helpviewer_keywords: ["Region::Translate"]
ms.assetid: 0dc16555-1df7-44b8-85fb-ff0963f3c68e
ms.date: 05/20/2019
ms.keywords: Region::Translate
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
 - Region::Translate
 - gdiplusheaders/Region::Translate
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdiplusheaders.h
api_name:
 - Region::Translate
---

# Region::Translate(INT,INT)


## -description

The **Region::Translate** method offsets this region by specified amounts in the horizontal and vertical directions.

## -parameters

### -param dx

Integer that specifies the amount to shift the region in the x direction.

### -param dy

Integer that specifies the amount to shift the region in the y direction.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

#### Examples

The following example creates a region from a path and fills it.
The code then translates the region and fills the translated region to show how the region has shifted.

```cpp
VOID Example_Translate(HDC hdc)
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

   // Translate the region.
   INT dx = 100;
   INT dy = 60;
   pathRegion.Translate(dx, dy);
   graphics.FillRegion(&solidBrush, &pathRegion);
}
```

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a>

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>

<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>

<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-region-transform">Region::Transform</a>
