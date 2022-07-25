---
UID: NF:gdipluspath.PathGradientBrush.GetCenterColor
title: PathGradientBrush::GetCenterColor (gdipluspath.h)
description: The PathGradientBrush::GetCenterColor method gets the color of the center point of this path gradient brush.
helpviewer_keywords: ["GetCenterColor","GetCenterColor method [GDI+]","GetCenterColor method [GDI+]","PathGradientBrush class","PathGradientBrush class [GDI+]","GetCenterColor method","PathGradientBrush.GetCenterColor","PathGradientBrush::GetCenterColor","_gdiplus_CLASS_PathGradientBrush_GetCenterColor_color_","gdiplus._gdiplus_CLASS_PathGradientBrush_GetCenterColor_color_"]
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_GetCenterColor_color_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushmethods\getcentercolor.htm
ms.date: 12/05/2018
ms.keywords: GetCenterColor, GetCenterColor method [GDI+], GetCenterColor method [GDI+],PathGradientBrush class, PathGradientBrush class [GDI+],GetCenterColor method, PathGradientBrush.GetCenterColor, PathGradientBrush::GetCenterColor, _gdiplus_CLASS_PathGradientBrush_GetCenterColor_color_, gdiplus._gdiplus_CLASS_PathGradientBrush_GetCenterColor_color_
req.header: gdipluspath.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - PathGradientBrush::GetCenterColor
 - gdipluspath/PathGradientBrush::GetCenterColor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - PathGradientBrush.GetCenterColor
---

# PathGradientBrush::GetCenterColor


## -description

The <b>PathGradientBrush::GetCenterColor</b> method gets the color of the center point of this path gradient brush.

## -parameters

### -param color [out]

Type: <b><a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a> object that receives the color of the center point.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

By default, the center point of a 
				<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a> object is the centroid of the brush's boundary path, but you can set the center point to any location, inside or outside the path, by calling the 
				<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)">PathGradientBrush::SetCenterPoint Methods</a> method of the 
				<b>PathGradientBrush</b> object.


#### Examples



The following example creates a 
						<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a> object and uses it to fill an ellipse. Then the code calls the <b>PathGradientBrush::GetCenterColor</b> method of the 
						<b>PathGradientBrush</b> object to obtain the center color.


```cpp
VOID Example_GetCenterColor(HDC hdc)
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
   int count = 1;
   pthGrBrush.SetSurroundColors(colors, &count);

   // Fill the ellipse with the path gradient brush.
   graphics.FillEllipse(&pthGrBrush, 0, 0, 200, 100);

   // Obtain information about the path gradient brush.
   Color color;
   pthGrBrush.GetCenterColor(&color);

   // Fill a rectangle with the retrieved color.
   SolidBrush solidBrush(color);
   graphics.FillRectangle(&solidBrush, 0, 120, 200, 30);
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>



<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="/windows/desktop/gdiplus/-gdiplus-filling-a-shape-with-a-color-gradient-use">Filling a Shape with a Color Gradient</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-getcenterpoint(outpoint)">PathGradientBrush::GetCenterPoint Methods</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcentercolor">PathGradientBrush::SetCenterColor</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)">PathGradientBrush::SetCenterPoint Methods</a>