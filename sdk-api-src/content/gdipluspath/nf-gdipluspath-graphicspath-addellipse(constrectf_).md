---
UID: NF:gdipluspath.GraphicsPath.AddEllipse(constRectF&)
title: GraphicsPath::AddEllipse
description: The GraphicsPath::AddEllipse method adds an ellipse to this path. (overload 2/4)
tech.root: gdiplus
helpviewer_keywords: ["GraphicsPath::AddEllipse"]
ms.assetid: 9acdbd19-0354-4728-a96c-611b93cbffe5
ms.date: 05/13/2019
ms.keywords: GraphicsPath::AddEllipse
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
 - GraphicsPath::AddEllipse
 - gdipluspath/GraphicsPath::AddEllipse
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdipluspath.h
api_name:
 - GraphicsPath::AddEllipse
---

# GraphicsPath::AddEllipse


## -description

The **GraphicsPath::AddEllipse** method adds an ellipse to this path.

## -parameters

### -param rect

Reference to a rectangle that bounds the ellipse.

## -returns

**Type:** <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

A <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object stores an ellipse as a sequence of four connected Bézier splines.
The **GraphicsPath** object does not store the upper-left corner, width, and height of the ellipse's bounding rectangle.

#### Examples

The following example creates a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object path, adds an ellipse to path, and then draws path.

```cpp
VOID Example_AddEllipse(HDC hdc)
{
   Graphics graphics(hdc); 
   RectF rect(20.0f, 20.0f, 200.0f, 100.0f);

   GraphicsPath path;
   path.AddEllipse(rect);

   // Draw the path.
   Pen pen(Color(255, 255, 0, 0));
   graphics.DrawPath(&pen, &path);
}
```

## -see-also

<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-addarc(inconstrect__inreal_inreal)">AddArc Methods</a>

<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-addellipse(inconstrect_)">AddEllipse Methods</a>

<a href="/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>

<a href="/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>

<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>

<a href="/windows/desktop/gdiplus/-gdiplus-ellipses-and-arcs-about">Ellipses and Arcs</a>

<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>

<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a>
