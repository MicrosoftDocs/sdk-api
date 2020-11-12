---
UID: NF:gdipluspath.GraphicsPath.IsOutlineVisible(constPointF&,constPen,constGraphics)
title: GraphicsPath::IsOutlineVisible
description: The GraphicsPath::IsOutlineVisible method determines whether a specified point touches the outline of a path.
tech.root: gdiplus
helpviewer_keywords: ["GraphicsPath::IsOutlineVisible"]
ms.assetid: f80b0cd2-0c6c-4fa9-9567-5383750689e8
ms.date: 05/13/2019
ms.keywords: GraphicsPath::IsOutlineVisible
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
 - GraphicsPath::IsOutlineVisible
 - gdipluspath/GraphicsPath::IsOutlineVisible
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdipluspath.h
api_name:
 - GraphicsPath::IsOutlineVisible
---

# GraphicsPath::IsOutlineVisible


## -description

The **GraphicsPath::IsOutlineVisible** method determines whether a specified point touches the outline of this path when the path is drawn by a specified <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object and a specified pen.

## -parameters

### -param point

Reference to the point to be tested.

### -param pen

Pointer to a **Pen** object.
This method determines whether the test point touches the path outline that would be drawn by this pen.
More points will touch an outline drawn by a wide pen than will touch an outline drawn by a narrow pen.

### -param g

Optional.
Pointer to a **Graphics** object that specifies a world-to-device transformation.
If the value of this parameter is **NULL**, the test is done in world coordinates; otherwise, the test is done in device coordinates.
The default value is **NULL**.

## -returns

If the test point touches the outline of this path, this method returns **TRUE**; otherwise, it returns **FALSE**.

## -remarks

#### Examples

The following example creates an elliptical path and draws that path with a wide yellow pen.
Then the code tests each point in an array to see whether the point touches the outline (as it would be drawn by the wide yellow pen) of the path.
Points that touch the outline are painted green, and points that don't touch the outline are painted red.

```cpp
VOID Example_IsOutlineVisibleExample(HDC hdc)
{
   Graphics graphics(hdc);

   INT j;
   Pen yellowPen(Color(255, 255, 255, 0), 20);
   SolidBrush brush(Color(255, 255, 0,  0));

   // Create and draw a path.
   GraphicsPath path;
   path.AddEllipse(50, 50, 200, 100);
   graphics.DrawPath(&yellowPen, &path);

   // Create an array of three points, and determine whether each
   // point in the array touches the outline of the path.
   // If a point touches the outline, paint it green.
   // If a point does not touch the outline, paint it red.
   PointF[] = {
      PointF(230, 138),
      PointF(100, 120),
      PointF(150, 170)};

   for(j = 0; j <= 2; ++j)
   {
      if(path.IsOutlineVisible(points[j], &yellowPen, NULL))
         brush.SetColor(Color(255, 0, 255,  0));
      else
         brush.SetColor(Color(255, 255, 0,  0));

      graphics.FillEllipse(&brush, points[j].X - 3.0f, points[j].Y - 3.0f, 6.0f, 6.0f);
   }
}

Color(255, 255, 0,  0)Color(255, 255, 0,  0)
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>

<a href="/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>

<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>

<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>

<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>

<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-isoutlinevisible(inconstpoint__inconstpen_inconstgraphics)">IsOutlineVisible Methods</a>

<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-isvisible(inconstpoint__inconstgraphics)">IsVisible Methods</a>

<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>

<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>

<a href="/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a>

<a href="/windows/desktop/gdiplus/-gdiplus-setting-pen-width-and-alignment-use">Setting Pen Width and Alignment</a>