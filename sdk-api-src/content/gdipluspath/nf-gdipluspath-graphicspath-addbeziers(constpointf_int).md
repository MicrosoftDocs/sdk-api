---
UID: NF:gdipluspath.GraphicsPath.AddBeziers(constPointF,INT)
title: GraphicsPath::AddBeziers
description: The GraphicsPath::AddBeziers method adds a sequence of connected Bezier splines to the current figure of this path.
tech.root: gdiplus
helpviewer_keywords: ["GraphicsPath::AddBeziers"]
ms.assetid: 62a632ff-1282-46e4-a130-809e4bb51c97
ms.date: 05/13/2019
ms.keywords: GraphicsPath::AddBeziers
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
 - GraphicsPath::AddBeziers
 - gdipluspath/GraphicsPath::AddBeziers
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdipluspath.h
api_name:
 - GraphicsPath::AddBeziers
---

# GraphicsPath::AddBeziers


## -description

The **GraphicsPath::AddBeziers** method adds a sequence of connected Bézier splines to the current figure of this path.

## -parameters

### -param points

Pointer to an array of starting points, ending points, and control points for the connected splines.
The first spline is constructed from the first point through the fourth point in the array and uses the second and third points as control points.
Each subsequent spline in the sequence needs exactly three more points: the ending point of the previous spline is used as the starting point, the next two points in the sequence are control points, and the third point is the ending point.

### -param count

Integer that specifies the number of elements in the points array.

## -returns

**Type:** <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

#### Examples

The following example creates a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object path, adds a sequence of two connected Bézier splines to path, closes the current figure (the only figure in this case), and then draws path.

```cpp
VOID Example_AddBeziers(HDC hdc)
{
   Graphics graphics(hdc);
   GraphicsPath  path;

   Point pts[] = {Point(50,50),
                  Point(60,20),
                  Point(70,100),
                  Point(80,50),
                  Point(120,40),
                  Point(150,80),
                  Point(170,30)};

   path.AddBeziers(pts, 7);
   path.CloseFigure();

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