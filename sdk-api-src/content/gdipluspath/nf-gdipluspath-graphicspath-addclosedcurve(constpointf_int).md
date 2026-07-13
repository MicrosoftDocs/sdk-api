---
UID: NF:gdipluspath.GraphicsPath.AddClosedCurve(constPointF,INT)
title: GraphicsPath::AddClosedCurve
description: The GraphicsPath::AddClosedCurve method adds a closed cardinal spline to this path. (overload 1/4)
tech.root: gdiplus
helpviewer_keywords: ["GraphicsPath::AddClosedCurve"]
ms.assetid: cd2aaebd-da69-4664-ae8b-c559bb510913
ms.date: 05/13/2019
ms.keywords: GraphicsPath::AddClosedCurve
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
 - GraphicsPath::AddClosedCurve
 - gdipluspath/GraphicsPath::AddClosedCurve
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdipluspath.h
api_name:
 - GraphicsPath::AddClosedCurve
---

# GraphicsPath::AddClosedCurve


## -description

The **GraphicsPath::AddClosedCurve** method adds a closed cardinal spline to this path.

## -parameters

### -param points

Pointer to an array of points that define the cardinal spline.
The cardinal spline is a curve that passes through each point in the array.

### -param count

Integer that specifies the number of elements in the points array.

## -returns

**Type:** <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

You should keep a copy of the points array if those points will be needed later.
The **GraphicsPath** object does not store the points passed to the **GraphicsPath::AddClosedCurve** method; instead, it converts the cardinal spline to a sequence of Bézier splines and stores the points that define those Bézier splines.
You cannot retrieve the original array of points from the **GraphicsPath** object.

#### Examples

The following example creates a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object path, adds a closed cardinal spline to path, and then draws path.

```cpp
VOID Example_AddClosedCurve(HDC hdc)
{
   Graphics graphics(hdc);

   PointF pts[] = {PointF(50.0f,50.0f),
                   PointF(60.0f,20.0f),
                   PointF(70.0f,100.0f),
                   PointF(80.0f,50.0f)};

   GraphicsPath path;
   path.AddClosedCurve(pts, 4);

   // Draw the path.
   Pen pen(Color(255, 255, 0, 0));
   graphics.DrawPath(&pen, &path);
}
```

## -see-also

<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-addbezier(inconstpoint__inconstpoint__inconstpoint__inconstpoint_)">AddBezier Methods</a>

<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-addbeziers(inconstpoint_inint)">AddBeziers Methods</a>

<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpointf_inint_inint_inint_inreal)">AddCurve Methods</a>

<a href="/windows/desktop/gdiplus/-gdiplus-bezier-splines-about">Bézier Splines</a>

<a href="/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>

<a href="/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>

<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>

<a href="/windows/desktop/gdiplus/-gdiplus-drawing-bezier-splines-use">Drawing Bézier Splines</a>

<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>

<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>
