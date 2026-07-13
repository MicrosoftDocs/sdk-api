---
UID: NF:gdipluspath.GraphicsPath.AddLines(constPointF,INT)
title: GraphicsPath::AddLines
description: The GraphicsPath::AddLines method adds a sequence of connected lines to the current figure of this path. (overload 1/2)
tech.root: gdiplus
helpviewer_keywords: ["GraphicsPath::AddLines"]
ms.assetid: 8b530334-98d8-4f73-88d5-e585c4b8e8ea
ms.date: 05/13/2019
ms.keywords: GraphicsPath::AddLines
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
 - GraphicsPath::AddLines
 - gdipluspath/GraphicsPath::AddLines
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdipluspath.h
api_name:
 - GraphicsPath::AddLines
---

# GraphicsPath::AddLines


## -description

The **GraphicsPath::AddLines** method adds a sequence of connected lines to the current figure of this path.

## -parameters

### -param points

Pointer to an array of points that specify the starting and ending points of the lines.
The first point in the array is the starting point of the first line, and the last point in the array is the ending point of the last line.
Each of the other points serves as ending point for one line and starting point for the next line.

### -param count

Integer that specifies the number of elements in the points array.

## -returns

**Type:** <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

#### Examples

The following example creates a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object path, adds a sequence of four connected lines to path, and then draws path.

```cpp
VOID Example_AddLines(HDC hdc)
{
   Graphics graphics(hdc);

   PointF pts[] = {PointF(20.0f, 20.0f),
                   PointF(30.0f, 30.0f),
                   PointF(40.0f, 25.0f),
                   PointF(50.0f, 30.0f),
                   PointF(60.0f, 20.0f)};

   GraphicsPath path;
   path.AddLines(pts, 5);

   // Draw the path.
   Pen pen(Color(255, 255, 0, 0));
   graphics.DrawPath(&pen, &path);
}
```

## -see-also

<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-addline(inconstpoint__inconstpoint_)">AddLine Methods</a>

<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-addlines(inconstpoint_inint)">AddLines Methods</a>

<a href="/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>

<a href="/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>

<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>

<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>

<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>

<a href="/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a>

<a href="/windows/desktop/gdiplus/-gdiplus-using-a-pen-to-draw-lines-and-rectangles-use">Using a Pen to Draw Lines and Rectangles</a>
