---
UID: NF:gdipluspath.PathGradientBrush.GetRectangle(RectF)
title: PathGradientBrush::GetRectangle
description: The PathGradientBrush::GetRectangle method gets the smallest rectangle that encloses the boundary path of this path gradient brush. (overload 2/2)
tech.root: gdiplus
helpviewer_keywords: ["PathGradientBrush::GetRectangle"]
ms.assetid: da6ff6c8-4be9-46fe-8509-5e72b2feab71
ms.date: 05/13/2019
ms.keywords: PathGradientBrush::GetRectangle
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
 - PathGradientBrush::GetRectangle
 - gdipluspath/PathGradientBrush::GetRectangle
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdipluspath.h
api_name:
 - PathGradientBrush::GetRectangle
---

# PathGradientBrush::GetRectangle


## -description

The **PathGradientBrush::GetRectangle** method gets the smallest rectangle that encloses the boundary path of this path gradient brush.

## -parameters

### -param rect

Pointer to a **RectF** object that receives the bounding rectangle.

## -returns

**Type:** <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

#### Examples

The following example creates a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a> object based on a polygon that is defined by four points.
The code calls the **PathGradientBrush::GetRectangle** method of the PathGradientBrush object to obtain the smallest rectangle that encloses the brush's boundary path.
The code calls the **Graphics::FillRectangle** method of a Graphics object, passing the address of the **PathGradientBrush** object and a reference to the brush's bounding rectangle.
That call fills only the portion of the bounding rectangle that is inside the brush's boundary path.
Finally the code draws the outline of the bounding rectangle.

```cpp
VOID Example_GetRect(HDC hdc)
{
   Graphics graphics(hdc);
   Pen pen(Color(255, 0, 0, 0));

   // Create a path gradient brush based on an array of points.
   Point points[] = {
      Point(30, 20),
      Point(150, 40),
      Point(100, 100),
      Point(60, 200) };

   PathGradientBrush pthGrBrush(points, 4);

   // Obtain information about the path gradient brush.
   RectF rect;
   pthGrBrush.GetRectangle(&rect);

   graphics.FillRectangle(&pthGrBrush, rect);
   graphics.DrawRectangle(&pen, rect);
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>

<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>

<a href="/windows/desktop/gdiplus/-gdiplus-filling-a-shape-with-a-color-gradient-use">Filling a Shape with a Color Gradient</a>

<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>

<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a>

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a>
