---
UID: NF:gdipluspath.PathGradientBrush.GetCenterPoint(PointF)
title: PathGradientBrush::GetCenterPoint
description: The PathGradientBrush::GetCenterPoint method gets the center point of this path gradient brush. (overload 2/2)
tech.root: gdiplus
helpviewer_keywords: ["PathGradientBrush::GetCenterPoint"]
ms.assetid: 80e265c4-6f87-4a3f-b198-b2857a0aa182
ms.date: 05/13/2019
ms.keywords: PathGradientBrush::GetCenterPoint
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
 - PathGradientBrush::GetCenterPoint
 - gdipluspath/PathGradientBrush::GetCenterPoint
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdipluspath.h
api_name:
 - PathGradientBrush::GetCenterPoint
---

# PathGradientBrush::GetCenterPoint


## -description

The **PathGradientBrush::GetCenterPoint** method gets the center point of this path gradient brush.

## -parameters

### -param point

Pointer to a PointF object that receives the center point.

## -returns

**Type:** <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

By default, the center point of a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a> object is at the centroid of the brush's boundary path, but you can set the center point to any location, inside or outside the path, by calling the **SetCenterPoint** method of the **PathGradientBrush** object.

#### Examples

The following example demonstrates several methods of the **PathGradientBrush** class including **PathGradientBrush::GetCenterPoint** and **PathGradientBrush::SetCenterColor**.
The code creates a **PathGradientBrush** object and then sets the brush's center color and boundary color.
The code calls the **PathGradientBrush::GetCenterPoint** method to determine the center point of the path gradient and then draws a line from the origin to that center point.

```cpp
VOID Example_GetCenterPoint(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a path that consists of a single ellipse.
   GraphicsPath path;
   path.AddEllipse(0, 0, 200, 100);

   // Use the path to construct a brush.
   PathGradientBrush pthGrBrush(&path);

   // Set the color at the center of the path to blue.
   pthGrBrush.SetCenterColor(Color(255, 0, 0, 255));

   // Set the color along the entire boundary of the path to aqua.
   Color colors[] = {Color(255, 0, 255, 255)};
   INT count = 1;
   pthGrBrush.SetSurroundColors(colors, &count);

   // Fill the ellipse with the path gradient brush.
   graphics.FillEllipse(&pthGrBrush, 0, 0, 200, 100);

   // Obtain information about the path gradient brush.
   PointF centerPoint;
   pthGrBrush.GetCenterPoint(&centerPoint);

   // Draw a line from the origin to the center of the ellipse.
   Pen pen(Color(255, 0, 255, 0));
   graphics.DrawLine(&pen, PointF(0, 0), centerPoint);  
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>

<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>

<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>

<a href="/windows/desktop/gdiplus/-gdiplus-filling-a-shape-with-a-color-gradient-use">Filling a Shape with a Color Gradient</a>

<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a>

<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-getcentercolor">PathGradientBrush::GetCenterColor</a>

<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcentercolor">PathGradientBrush::SetCenterColor</a>

<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)">PathGradientBrush::SetCenterPoint Methods</a>
