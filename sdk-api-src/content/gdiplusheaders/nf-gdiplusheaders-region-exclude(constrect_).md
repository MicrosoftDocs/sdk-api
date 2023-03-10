---
UID: NF:gdiplusheaders.Region.Exclude(constRect&)
title: Region::Exclude
description: The Region::Exclude method updates a region that does not intersect the specified rectangle's interior.
tech.root: gdiplus
helpviewer_keywords: ["Region::Exclude"]
ms.assetid: b8a1fd06-45d5-426d-9582-8d5e837d1824
ms.date: 05/20/2019
ms.keywords: Region::Exclude
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
 - Region::Exclude
 - gdiplusheaders/Region::Exclude
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdiplusheaders.h
api_name:
 - Region::Exclude
---

# Region::Exclude(Rect&)


## -description

The **Region::Exclude** method updates this region to the portion of itself that does not intersect the specified rectangle's interior.

## -parameters

### -param rect

Reference to a rectangle to use to update this <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a> object.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

#### Examples

The following example creates a region from a path and then uses a rectangle to update the region.

```cpp
VOID Example_ExcludeRect(HDC hdc)
{
   Graphics graphics(hdc);

   Point points[] = {
      Point(110, 20),
      Point(120, 30),
      Point(100, 60),
      Point(120, 70),
      Point(150, 60),
      Point(140, 10)};

   Rect rect(65, 15, 70, 45);

   GraphicsPath path;
   SolidBrush solidBrush(Color(255, 255, 0, 0));

   path.AddClosedCurve(points, 6);

   // Create a region from a path.
   Region pathRegion(&path);

   // Exclude a rectangle from the path region.
   pathRegion.Exclude(rect);

   graphics.FillRegion(&solidBrush, &pathRegion);
}
```

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a>

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>

<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>