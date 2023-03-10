---
UID: NF:gdipluspath.PathGradientBrush.GetInterpolationColors
title: PathGradientBrush::GetInterpolationColors (gdipluspath.h)
description: The PathGradientBrush::GetInterpolationColors method gets the preset colors and blend positions currently specified for this path gradient brush.
helpviewer_keywords: ["GetInterpolationColors","GetInterpolationColors method [GDI+]","GetInterpolationColors method [GDI+]","PathGradientBrush class","PathGradientBrush class [GDI+]","GetInterpolationColors method","PathGradientBrush.GetInterpolationColors","PathGradientBrush::GetInterpolationColors","_gdiplus_CLASS_PathGradientBrush_GetInterpolationColors_presetColors_blendPositions_count_","gdiplus._gdiplus_CLASS_PathGradientBrush_GetInterpolationColors_presetColors_blendPositions_count_"]
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_GetInterpolationColors_presetColors_blendPositions_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushmethods\getinterpolationcolors_50presetcolors_blendpositions_count.htm
ms.date: 12/05/2018
ms.keywords: GetInterpolationColors, GetInterpolationColors method [GDI+], GetInterpolationColors method [GDI+],PathGradientBrush class, PathGradientBrush class [GDI+],GetInterpolationColors method, PathGradientBrush.GetInterpolationColors, PathGradientBrush::GetInterpolationColors, _gdiplus_CLASS_PathGradientBrush_GetInterpolationColors_presetColors_blendPositions_count_, gdiplus._gdiplus_CLASS_PathGradientBrush_GetInterpolationColors_presetColors_blendPositions_count_
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
 - PathGradientBrush::GetInterpolationColors
 - gdipluspath/PathGradientBrush::GetInterpolationColors
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
 - PathGradientBrush.GetInterpolationColors
---

# PathGradientBrush::GetInterpolationColors


## -description

The <b>PathGradientBrush::GetInterpolationColors</b> method gets the preset colors and blend positions currently specified for this path gradient brush.

## -parameters

### -param presetColors [out]

Type: <b><a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>*</b>

Pointer to an array that receives the preset colors. A color of a given index in the 
					<i>presetColors</i> array corresponds to the blend position of that same index in the 
					<i>blendPositions</i> array.

### -param blendPositions [out]

Type: <b>REAL*</b>

Pointer to an array that receives the blend positions. Each blend position is a number from 0 through 1, where 0 indicates the boundary of the gradient and 1 indicates the center point. A blend position between 0 and 1 indicates the set of all points that are a certain fraction of the distance from the boundary to the center point. For example, a blend position of 0.7 indicates the set of all points that are 70 percent of the way from the boundary to the center point.

### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the 
					<i>presetColors</i> array. This is the same as the number of elements in the 
					<i>blendPositions</i> array.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

A simple path gradient brush has two colors: a boundary color and a center color. When you paint with such a brush, the color changes gradually from the boundary color to the center color as you move from the boundary path to the center point. You can create a more complex gradient by specifying an array of preset colors and an array of blend positions. 

Before you call the <b>PathGradientBrush::GetInterpolationColors</b> method, you must allocate two buffers: one to hold the array of preset colors and one to hold the array of blend positions. You can call the <a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-getinterpolationcolorcount">PathGradientBrush::GetInterpolationColorCount</a> method of the 
				<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a> object to determine the required size of those buffers. The size of the color buffer is the return value of <b>PathGradientBrush::GetInterpolationColorCount</b> multiplied by 
				<b>sizeof</b>(<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>). The size of the position buffer is the value of <b>PathGradientBrush::GetInterpolationColorCount</b> multiplied by 
				<b>sizeof</b>(
				<b>REAL</b>).


#### Examples



The following example creates a 
						<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a> object from a triangular path. The code sets the preset colors to red, blue, and aqua and sets the blend positions to 0, 0.6, and 1. The code calls the <a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-getinterpolationcolorcount">PathGradientBrush::GetInterpolationColorCount</a> method of the 
						<b>PathGradientBrush</b> object to obtain the number of preset colors currently set for the brush. Next, the code allocates two buffers: one to hold the array of preset colors, and one to hold the array of blend positions. The call to the <b>PathGradientBrush::GetInterpolationColors</b> method of the 
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



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-getinterpolationcolorcount">PathGradientBrush::GetInterpolationColorCount</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setinterpolationcolors">PathGradientBrush::SetInterpolationColors</a>