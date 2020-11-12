---
UID: NF:gdiplusheaders.Region.Complement(constRect&)
title: Region::Complement
description: The Region::Complement method updates a region that does not intersect this region.
tech.root: gdiplus
helpviewer_keywords: ["Region::Complement"]
ms.assetid: a83d400f-0a3d-4486-a9a7-831455908ff8
ms.date: 05/20/2019
ms.keywords: Region::Complement
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
 - Region::Complement
 - gdiplusheaders/Region::Complement
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdiplusheaders.h
api_name:
 - Region::Complement
---

# Region::Complement(Rect&amp;)


## -description

The **Region::Complement** method updates this region to the portion of the specified rectangle's interior that does not intersect this region.

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
VOID Example_ComplementRect(HDC hdc)
{
   Graphics graphics(hdc);

   SolidBrush solidBrush(Color(255, 255, 0, 0));

   Point points[] = {
      Point(110, 20),
      Point(120, 30),
      Point(100, 60),
      Point(120, 70),
      Point(150, 60),
      Point(140, 10)};

   Rect rect(65, 15, 70, 45);

   GraphicsPath path;

   path.AddClosedCurve(points, 6);

   // Create a region from a path.
   Region region(&path); 

   // Update the region so that it consists of all points inside the 
   // rectangle but outside the path region.
   region.Complement(rect);

   graphics.FillRegion(&solidBrush, &region);
}
```

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a>

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>

<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>