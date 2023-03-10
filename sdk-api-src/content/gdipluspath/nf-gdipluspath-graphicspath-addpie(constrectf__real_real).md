---
UID: NF:gdipluspath.GraphicsPath.AddPie(constRectF&,REAL,REAL)
title: GraphicsPath::AddPie
description: The GraphicsPath::AddPie method adds a pie to this path. (overload 4/4)
tech.root: gdiplus
helpviewer_keywords: ["GraphicsPath::AddPie"]
ms.assetid: 6c8aeb29-caa6-4bfc-85bd-c873f8b93837
ms.date: 05/13/2019
ms.keywords: GraphicsPath::AddPie
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
 - GraphicsPath::AddPie
 - gdipluspath/GraphicsPath::AddPie
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdipluspath.h
api_name:
 - GraphicsPath::AddPie
---

# GraphicsPath::AddPie


## -description

The **GraphicsPath::AddPie** method adds a pie to this path.
An arc is a portion of an ellipse, and a pie is a portion of the area enclosed by an ellipse.
A pie is bounded by an arc and two lines (edges) that go from the center of the ellipse to the endpoints of the arc.

## -parameters

### -param rect

Reference to a rectangle that bounds the ellipse that bounds the pie.

### -param startAngle

Real number that specifies the clockwise angle, in degrees, between the horizontal axis of the ellipse and the starting point of the arc that defines the pie.

### -param sweepAngle

Real number that specifies the clockwise angle, in degrees, between the starting and ending points of the arc that defines the pie.

## -returns

**Type:** <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

#### Examples

The following example creates a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object path, adds a pie to path, and then draws path.

```cpp
VOID Example_AddPie(HDC hdc)
{
   Graphics graphics(hdc); 

   RectF rect(50.0f, 50.0f, 100.0f, 100.0f);

   GraphicsPath path;
   path.AddPie(rect, 20.0f, 45.0f);

   // Draw the path.
   Pen pen(Color(255, 255, 0, 0));
   graphics.DrawPath(&pen, &path);

   graphics.DrawPath(&pen, &path);
}
```

## -see-also

<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-addarc(inconstrect__inreal_inreal)">AddArc Methods</a>

<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-addpie(inconstrect__inreal_inreal)">AddPie Methods</a>

<a href="/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>

<a href="/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>

<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>

<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inconstrectf__inreal_inreal)">DrawArc Methods</a>

<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpie(inconstpen_inconstrect__inreal_inreal)">DrawPie Methods</a>

<a href="/windows/desktop/gdiplus/-gdiplus-ellipses-and-arcs-about">Ellipses and Arcs</a>

<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>

<a href="/windows/desktop/gdiplus/-gdiplus-open-and-closed-curves-about">Open and Closed Curves</a>

<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a>
