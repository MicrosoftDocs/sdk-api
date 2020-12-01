---
UID: NF:gdipluspath.GraphicsPath.AddRectangles(constRectF,INT)
title: GraphicsPath::AddRectangles
description: The GraphicsPath::AddRectangles method adds a sequence of rectangles to this path.
tech.root: gdiplus
helpviewer_keywords: ["GraphicsPath::AddRectangles"]
ms.assetid: 9f5e91b9-bf02-4f4b-bb33-7a2dae2e1306
ms.date: 05/13/2019
ms.keywords: GraphicsPath::AddRectangles
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
 - GraphicsPath::AddRectangles
 - gdipluspath/GraphicsPath::AddRectangles
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdipluspath.h
api_name:
 - GraphicsPath::AddRectangles
---

# GraphicsPath::AddRectangles


## -description

The **GraphicsPath::AddRectangles** method adds a sequence of rectangles to this path.

## -parameters

### -param rects

Pointer to an array of rectangles that will be added to the path.

### -param count

Integer that specifies the number of elements in the rects array.

## -returns

**Type:** <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

#### Examples

The following example creates a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object path, adds two rectangles to path, and then draws path.

```cpp
VOID Example_AddRectangles(HDC hdc)
{
   Graphics graphics(hdc);

   RectF rects[] = {RectF(20.0f, 20.0f, 100.0f, 50.0f),
                    RectF(30.0f, 30.0f, 50.0f, 100.0f)};

   GraphicsPath path;
   path.AddRectangles(rects, 2);

   // Draw the path.
   Pen pen(Color(255, 255, 0, 0));
   graphics.DrawPath(&pen, &path);
}
```

## -see-also

<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangle(inconstrect_)">AddRectangle Methods</a>

<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangles(inconstrect_int)">AddRectangles Methods</a>

<a href="/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>

<a href="/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>

<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>

<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>

<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>

<a href="/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a>

<a href="/windows/desktop/gdiplus/-gdiplus-using-a-pen-to-draw-lines-and-rectangles-use">Using a Pen to Draw Lines and Rectangles</a>