---
UID: NF:gdipluspath.GraphicsPath.AddRectangle(constRectF&)
title: GraphicsPath::AddRectangle
description: The GraphicsPath::AddRectangle method adds a rectangle to this path. (overload 2/2)
tech.root: gdiplus
helpviewer_keywords: ["GraphicsPath::AddRectangle"]
ms.assetid: 3b7288d2-c5b9-4b3b-be6f-218ad8511217
ms.date: 05/13/2019
ms.keywords: GraphicsPath::AddRectangle
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: gdipluspath.h
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
 - GraphicsPath::AddRectangle
 - gdipluspath/GraphicsPath::AddRectangle
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdipluspath.h
api_name:
 - GraphicsPath::AddRectangle
---

# GraphicsPath::AddRectangle


## -description

The **GraphicsPath::AddRectangle** method adds a rectangle to this path.

## -parameters

### -param rect

Reference to a rectangle to be added to the path.

## -returns

**Type:** <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

#### Examples

The following example creates a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object path, adds a rectangle to path, and then draws path.

```cpp
VOID Example_AddRectangle(HDC hdc)
{
   Graphics graphics(hdc);
   RectF rect(20.0f, 20.0f, 100.0f, 50.0f);

   GraphicsPath path;
   path.AddRectangle(rect);

   // Draw the path.
   Pen pen(Color(255, 255, 0, 0));
   graphics.DrawPath(&pen, &path);
}
```

## -see-also

<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-addpolygon(inconstpoint_inint)">AddPolygon Methods</a>

<a href="/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>

<a href="/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>

<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>

<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>

<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a>

<a href="/windows/desktop/gdiplus/-gdiplus-polygons-about">Polygons</a>
