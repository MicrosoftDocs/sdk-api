---
UID: NF:gdipluspath.GraphicsPath.AddArc(constRectF&,REAL,REAL)
title: GraphicsPath::AddArc
description: The GraphicsPath::AddArc method adds an elliptical arc to the current figure of this path. (overload 4/4)
tech.root: gdiplus
helpviewer_keywords: ["GraphicsPath::AddArc"]
ms.assetid: 2616a8ff-8193-413b-ab7f-56c0dd82c17b
ms.date: 05/13/2019
ms.keywords: GraphicsPath::AddArc
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
 - GraphicsPath::AddArc
 - gdipluspath/GraphicsPath::AddArc
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdipluspath.h
api_name:
 - GraphicsPath::AddArc
---

#  GraphicsPath::AddArc


## -description

The **GraphicsPath::AddArc** method adds an elliptical arc to the current figure of this path.

## -parameters

### -param rect

Reference to a rectangle that bounds the ellipse that contains the arc.

### -param startAngle

Real number that specifies the clockwise angle, in degrees, between the horizontal axis of the ellipse and the starting point of the arc.

### -param sweepAngle

Real number that specifies the clockwise angle, in degrees, between the starting point (startAngle) and the ending point of the arc.

## -returns

**Type:** <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

#### Examples

The following example creates a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object *path*, adds an arc to *path*, closes the arc, and then draws *path*.

```cpp
VOID AddArcExample(HDC hdc)
{
   Graphics graphics(hdc);
   RectF rect(20.0f, 20.0f, 50.0f, 100.0f);

   GraphicsPath path;
   path.AddArc(rect, 0.0f, 180.0f);
   path.CloseFigure();

   // Draw the path.
   Pen pen(Color(255, 255, 0, 0));
   graphics.DrawPath(&pen, &path);
}
```

## -see-also

<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-addarc(inconstrect__inreal_inreal)">AddArc Methods</a>

<a href="/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>

<a href="/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>

<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>

<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inconstrectf__inreal_inreal)">DrawArc Methods</a>

<a href="/windows/desktop/gdiplus/-gdiplus-ellipses-and-arcs-about">Ellipses and Arcs</a>

<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>

<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a>
