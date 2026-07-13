---
UID: NF:gdipluspath.GraphicsPath.GetBounds(RectF,constMatrix,constPen)
title: GraphicsPath::GetBounds
description: The GraphicsPath::GetBounds method gets a bounding rectangle for this path. (overload 2/2)
tech.root: gdiplus
helpviewer_keywords: ["GraphicsPath::GetBounds"]
ms.assetid: a6a44cf0-78a9-4a1c-95f8-06d2ac32339b
ms.date: 05/13/2019
ms.keywords: GraphicsPath::GetBounds
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
 - GraphicsPath::GetBounds
 - gdipluspath/GraphicsPath::GetBounds
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdipluspath.h
api_name:
 - GraphicsPath::GetBounds
---

# GraphicsPath::GetBounds


## -description

The **GraphicsPath::GetBounds** method gets a bounding rectangle for this path.

## -parameters

### -param bounds

Pointer to a **RectF** object that receives the bounding rectangle.

### -param matrix

Optional.
Pointer to a **Matrix** object that specifies a transformation to be applied to this path before the bounding rectangle is calculated.
This path is not permanently transformed; the transformation is used only during the process of calculating the bounding rectangle.
The default value is **NULL**.

### -param pen

Optional.
Pointer to a **Pen** object that influences the size of the bounding rectangle.
The bounding rectangle received in bounds will be large enough to enclose this path when the path is drawn with the pen specified by this parameter.
This ensures that the path is enclosed by the bounding rectangle even if the path is drawn with a wide pen.
The default value is **NULL**.

## -returns

**Type:** <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

The rectangle returned by this method might be larger than necessary to enclose the path as drawn by the specified pen.
The rectangle is calculated to allow for the pen's miter limit at sharp corners and to allow for the pen's end caps.

#### Examples

The following example creates a path that has one curve and one ellipse.
The code draws the path with a thick yellow pen and a thin black pen.
The **GraphicsPath::GetBounds** method receives the address of the thick yellow pen and calculates a bounding rectangle for the path.
Then the code draws the bounding rectangle.

```cpp

VOID GetBoundsExample(HDC hdc)
{
   Graphics graphics(hdc);
   Pen blackPen(Color(255, 0, 0, 0), 1);
   Pen yellowPen(Color(255, 255, 255, 0), 10);
   Pen redPen(Color(255, 255, 0, 0), 1);

   Point pts[] = {Point(120,120), 
                  Point(200,130), 
                  Point(150,200), 
                  Point(130,180)};

   // Create a path that has one curve and one ellipse.
   GraphicsPath path;
   path.AddClosedCurve(pts, 4);
   path.AddEllipse(120, 220, 100, 40);

   // Draw the path with a thick yellow pen and a thin black pen.
   graphics.DrawPath(&yellowPen, &path);
   graphics.DrawPath(&blackPen, &path);

   // Get the path's bounding rectangle.
   RectF rect;
   path.GetBounds(&rect, NULL, &yellowPen);
   graphics.DrawRectangle(&redPen, rect);  
}

Color(255, 0, 0, 0)Color(255, 255, 0,  0)
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>

<a href="/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>

<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>

<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>

<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>

<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>

<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a>
