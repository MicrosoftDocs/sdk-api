---
UID: NF:gdipluspath.PathGradientBrush.SetCenterPoint(constPointF&)
title: PathGradientBrush::SetCenterPoint
description: The PathGradientBrush::SetCenterPoint method sets the center point of this path gradient brush.
tech.root: gdiplus
helpviewer_keywords: ["PathGradientBrush::SetCenterPoint"]
ms.assetid: 3123b926-ce18-4d71-a1e9-24dd9ecbd50e
ms.date: 05/13/2019
ms.keywords: PathGradientBrush::SetCenterPoint
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
 - PathGradientBrush::SetCenterPoint
 - gdipluspath/PathGradientBrush::SetCenterPoint
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdipluspath.h
api_name:
 - PathGradientBrush::SetCenterPoint
---

# PathGradientBrush::SetCenterPoint


## -description

The **PathGradientBrush::SetCenterPoint** method sets the center point of this path gradient brush.
By default, the center point is at the centroid of the brush's boundary path, but you can set the center point to any location inside or outside the path.

## -parameters

### -param point

Reference to a **PointF** object that specifies the center point.

## -returns

**Type:** <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

#### Examples

The following example creates a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a> object based on an ellipse.
The code sets the center color to blue and sets the color along the boundary to aqua.
By default, the center point would be at the center of the ellipse (100, 50), but the call to the **PathGradientBrush::SetCenterPoint** method sets the center point to (180.5, 50.0).

```cpp
VOID Example_SetCenter(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a path that consists of a single ellipse.
   GraphicsPath path;
   path.AddEllipse(0, 0, 200, 100);

   // Use the path to construct a brush.
   PathGradientBrush pthGrBrush(&path);

   // Set the color at the center of the path to blue.
   pthGrBrush.SetCenterColor(Color(255, 0, 0, 255));

   // Set the center point.
   pthGrBrush.SetCenterPoint(PointF(180.5f, 50.0f));

   // Set the color along the entire boundary of the path to aqua.
   Color colors[] = {Color(255, 0, 255, 255)};
   INT count = 1;
   pthGrBrush.SetSurroundColors(colors, &count);

   graphics.FillRectangle(&pthGrBrush, 0, 0, 300, 300);
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>

<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>

<a href="/windows/desktop/gdiplus/-gdiplus-filling-a-shape-with-a-color-gradient-use">Filling a Shape with a Color Gradient</a>

<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>

<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a>

<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-getcentercolor">PathGradientBrush::GetCenterColor</a>

<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-getcenterpoint(outpoint)">PathGradientBrush::GetCenterPoint Methods</a>

<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcentercolor">PathGradientBrush::SetCenterColor</a>