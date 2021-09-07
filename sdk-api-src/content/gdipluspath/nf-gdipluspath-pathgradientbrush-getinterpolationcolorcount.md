---
UID: NF:gdipluspath.PathGradientBrush.GetInterpolationColorCount
title: PathGradientBrush::GetInterpolationColorCount (gdipluspath.h)
description: The PathGradientBrush::GetInterpolationColorCount method gets the number of preset colors currently specified for this path gradient brush.
helpviewer_keywords: ["GetInterpolationColorCount","GetInterpolationColorCount method [GDI+]","GetInterpolationColorCount method [GDI+]","PathGradientBrush class","PathGradientBrush class [GDI+]","GetInterpolationColorCount method","PathGradientBrush.GetInterpolationColorCount","PathGradientBrush::GetInterpolationColorCount","_gdiplus_CLASS_PathGradientBrush_GetInterpolationColorCount_","gdiplus._gdiplus_CLASS_PathGradientBrush_GetInterpolationColorCount_"]
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_GetInterpolationColorCount_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushmethods\getinterpolationcolorcount_80.htm
ms.date: 12/05/2018
ms.keywords: GetInterpolationColorCount, GetInterpolationColorCount method [GDI+], GetInterpolationColorCount method [GDI+],PathGradientBrush class, PathGradientBrush class [GDI+],GetInterpolationColorCount method, PathGradientBrush.GetInterpolationColorCount, PathGradientBrush::GetInterpolationColorCount, _gdiplus_CLASS_PathGradientBrush_GetInterpolationColorCount_, gdiplus._gdiplus_CLASS_PathGradientBrush_GetInterpolationColorCount_
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
 - PathGradientBrush::GetInterpolationColorCount
 - gdipluspath/PathGradientBrush::GetInterpolationColorCount
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
 - PathGradientBrush.GetInterpolationColorCount
---

# PathGradientBrush::GetInterpolationColorCount


## -description

The <b>PathGradientBrush::GetInterpolationColorCount</b> method gets the number of preset colors currently specified for this path gradient brush.



## -returns

Type: <b>INT</b>

This method returns the number of preset colors currently specified for this path gradient brush.

## -remarks

A simple path gradient brush has two colors: a boundary color and a center color. When you paint with such a brush, the color changes gradually from the boundary color to the center color as you move from the boundary path to the center point. You can create a more complex gradient by specifying an array of preset colors and an array of blend positions.

You can obtain the interpolation colors and interpolation positions currently set for a 
				<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a> object by calling the <a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-getinterpolationcolors">PathGradientBrush::GetInterpolationColors</a> method of that 
				<b>PathGradientBrush</b> object. Before you call the <b>PathGradientBrush::GetInterpolationColors</b> method, you must allocate two buffers: one to hold the array of interpolation colors and one to hold the array of interpolation positions. You can call the <b>PathGradientBrush::GetInterpolationColorCount</b> method of the 
				<b>PathGradientBrush</b> object to determine the required size of those buffers. The size of the color buffer is the return value of <b>GetInterpolationColorCount</b> multiplied by 
				<b>sizeof</b>(<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>). The size of the position buffer is the value of <b>PathGradientBrush::GetInterpolationColorCount</b> multiplied by 
				<b>sizeof</b>(
				<b>REAL</b>).


#### Examples



The following example creates a 
						<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a> object from a triangular path. The code sets the preset colors to red, blue, and aqua and sets the blend positions to 0, 0.6, and 1. The code calls the <b>PathGradientBrush::GetInterpolationColorCount</b> method of the 
						<b>PathGradientBrush</b> object to obtain the number of preset colors currently set for the brush. Next, the code allocates two buffers: one to hold the array of preset colors, and one to hold the array of blend positions. The call to the <a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-getinterpolationcolors">PathGradientBrush::GetInterpolationColors</a> method of the 
						<b>PathGradientBrush</b> object fills the buffers with the preset colors and the blend positions. Finally the code fills a small square with each of the preset colors.


```cpp
VOID Example_GetInterpColors(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a path gradient brush from an array of points, and
   // set the interpolation colors for that brush.

   Point points[] = {Point(100, 0), Point(200, 200), Point(0, 200)};
   PathGradientBrush pthGrBrush(points, 3);

   Color col[] = {
      Color(255, 255, 0, 0),     // red
      Color(255, 0, 0, 255),     // blue
      Color(255, 0, 255, 255)};  // aqua

   REAL pos[] = {
      0.0f,    // red at the boundary
      0.6f,    // blue 60 percent of the way from the boundary to the center
      1.0f};   // aqua at the center

   pthGrBrush.SetInterpolationColors(col, pos, 3);

   // Obtain information about the path gradient brush.
   INT colorCount = pthGrBrush.GetInterpolationColorCount();
   Color* colors = new Color[colorCount];
   REAL* positions = new REAL[colorCount];
   pthGrBrush.GetInterpolationColors(colors, positions, colorCount);

   // Fill a small square with each of the interpolation colors.
   SolidBrush solidBrush(Color(255, 255, 255, 255));

   for(INT j = 0; j < colorCount; ++j)
   {
      solidBrush.SetColor(colors[j]);
      graphics.FillRectangle(&solidBrush, 15*j, 0, 10, 10);
   }

   delete [] colors;
   delete [] positions; 
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>



<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="/windows/desktop/gdiplus/-gdiplus-filling-a-shape-with-a-color-gradient-use">Filling a Shape with a Color Gradient</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-getinterpolationcolors">PathGradientBrush::GetInterpolationColors</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setinterpolationcolors">PathGradientBrush::SetInterpolationColors</a>
