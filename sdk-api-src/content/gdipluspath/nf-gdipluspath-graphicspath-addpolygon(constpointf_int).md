---
UID: NF:gdipluspath.GraphicsPath.AddPolygon(constPointF,INT)
title: GraphicsPath::AddPolygon
description: The GraphicsPath::AddPolygon method adds a polygon to this path. (overload 1/2)
tech.root: gdiplus
helpviewer_keywords: ["GraphicsPath::AddPolygon"]
ms.assetid: f342c271-baba-4a21-97c0-592114cd996a
ms.date: 05/13/2019
ms.keywords: GraphicsPath::AddPolygon
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
 - GraphicsPath::AddPolygon
 - gdipluspath/GraphicsPath::AddPolygon
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdipluspath.h
api_name:
 - GraphicsPath::AddPolygon
---

# GraphicsPath::AddPolygon


## -description

The **GraphicsPath::AddPolygon** method adds a polygon to this path.

## -parameters

### -param points

Pointer to an array of points that specifies the vertices of the polygon.

### -param count

Integer that specifies the number of elements in the points array.

## -returns

**Type:** <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

The **GraphicsPath::AddPolygon** method is similar to the **AddLines** method.
The difference is that a polygon is an intrinsically closed figure, but a sequence of lines is not a closed figure unless you call **GraphicsPath::CloseFigure**.
When Windows GDI+ renders a path, each polygon in that path is closed; that is, the last vertex of the polygon is connected to the first vertex by a straight line.

#### Examples

The following example creates a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object path, adds a polygon to path, and then draws path.

```cpp
VOID Example_AddPolygon(HDC hdc)
{
   Graphics graphics(hdc);

   PointF pts[] = {PointF(20.0f, 20.0f),
                   PointF(120.0f, 20.0f),
                   PointF(120.0f, 70.0f)};

   GraphicsPath path;
   path.AddPolygon(pts, 3);

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
