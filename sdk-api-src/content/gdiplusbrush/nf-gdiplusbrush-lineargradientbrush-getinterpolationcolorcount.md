---
UID: NF:gdiplusbrush.LinearGradientBrush.GetInterpolationColorCount
title: LinearGradientBrush::GetInterpolationColorCount (gdiplusbrush.h)
description: The LinearGradientBrush::GetInterpolationColorCount method gets the number of colors currently set to be interpolated for this linear gradient brush.
helpviewer_keywords: ["GetInterpolationColorCount","GetInterpolationColorCount method [GDI+]","GetInterpolationColorCount method [GDI+]","LinearGradientBrush class","LinearGradientBrush class [GDI+]","GetInterpolationColorCount method","LinearGradientBrush.GetInterpolationColorCount","LinearGradientBrush::GetInterpolationColorCount","_gdiplus_CLASS_LinearGradientBrush_GetInterpolationColorCount_","gdiplus._gdiplus_CLASS_LinearGradientBrush_GetInterpolationColorCount_"]
old-location: gdiplus\_gdiplus_CLASS_LinearGradientBrush_GetInterpolationColorCount_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\lineargradientbrushclass\lineargradientbrushmethods\getinterpolationcolorcount.htm
ms.date: 12/05/2018
ms.keywords: GetInterpolationColorCount, GetInterpolationColorCount method [GDI+], GetInterpolationColorCount method [GDI+],LinearGradientBrush class, LinearGradientBrush class [GDI+],GetInterpolationColorCount method, LinearGradientBrush.GetInterpolationColorCount, LinearGradientBrush::GetInterpolationColorCount, _gdiplus_CLASS_LinearGradientBrush_GetInterpolationColorCount_, gdiplus._gdiplus_CLASS_LinearGradientBrush_GetInterpolationColorCount_
req.header: gdiplusbrush.h
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
 - LinearGradientBrush::GetInterpolationColorCount
 - gdiplusbrush/LinearGradientBrush::GetInterpolationColorCount
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
 - LinearGradientBrush.GetInterpolationColorCount
---

# LinearGradientBrush::GetInterpolationColorCount


## -description

The <b>LinearGradientBrush::GetInterpolationColorCount</b> method gets the number of colors currently set to be interpolated for this linear gradient brush.



## -returns

Type: <b>INT</b>

This method returns the number of colors to be interpolated for this linear gradient brush. If no colors have been set by using <a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-setinterpolationcolors">LinearGradientBrush::SetInterpolationColors</a>, or if invalid positions were passed to <b>LinearGradientBrush::SetInterpolationColors</b>, then <b>LinearGradientBrush::GetInterpolationColorCount</b> returns 0.

## -remarks

A simple linear gradient brush has two colors: a color at the starting boundary and a color at the ending boundary. When you paint with such a brush, the color changes gradually from the starting color to the ending color as you move from the starting boundary to the ending boundary. You can create a more complex gradient by using the <a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-setinterpolationcolors">LinearGradientBrush::SetInterpolationColors</a> method to specify an array of colors and their corresponding blend positions to be interpolated for this linear gradient brush. 

You can obtain the colors and blend positions currently set for a linear gradient brush by calling its <a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-getinterpolationcolors">LinearGradientBrush::GetInterpolationColors</a> method. Before you call the <b>LinearGradientBrush::GetInterpolationColors</b> method, you must allocate two buffers: one to hold the array of colors and one to hold the array of blend positions. You can call the <b>LinearGradientBrush::GetInterpolationColorCount</b> method to determine the required size of those buffers. The size of the colors buffer is the return value of <b>LinearGradientBrush::GetInterpolationColorCount</b> multiplied by 
				<b>sizeof</b>(<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>). The size of the blend positions buffer is the value of <b>LinearGradientBrush::GetInterpolationColorCount</b> multiplied by 
				<b>sizeof</b>(
				<b>REAL</b>).


#### Examples



The following example sets the colors to be interpolated for this linear gradient brush to red, blue, and green and sets the blend positions to 0, 0.3, and 1. The code calls the <b>LinearGradientBrush::GetInterpolationColorCount</b> method of a 
						<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush">LinearGradientBrush</a> object to obtain the number of colors currently set to be interpolated for the brush. Next, the code gets the colors and their positions. Then, the code fills a small rectangle with each color.


```cpp
VOID Example_GetInterpColors(HDC hdc)
{
   Graphics myGraphics(hdc);

   // Create a linear gradient brush, and set the colors to be interpolated.
   Color col[] = {
      Color(255, 255, 0, 0),   // red
      Color(255, 0, 0, 255),   // blue
      Color(255, 0, 255, 0)};  // green

   REAL pos[] = {
      0.0f,   // red at the left edge
      0.3f,   // blue at 30 percent of the distance from 
              // left edge to right edge
      1.0f};  // green at the right edge

   LinearGradientBrush linGrBrush(
      Point(0, 0), 
      Point(100, 0),
      Color(255, 0, 0, 0),         // black
      Color(255, 255, 255, 255));  // white

   linGrBrush.SetInterpolationColors(col, pos, 3);

   // Obtain information about the linear gradient brush.
   INT    colorCount = 0;
   Color* colors = NULL;
   REAL*  positions = NULL;

   // How many colors have been specified to be interpolated 
   // for this brush?
   colorCount = linGrBrush.GetInterpolationColorCount();

   // Allocate a buffer large enough to hold the set of colors.
   colors = new Color[colorCount];

   // Allocate a buffer to hold the relative positions of the colors.
   positions = REAL[colorCount];

   // Get the colors and their relative positions.
   linGrBrush.GetInterpolationColors(colors, positions, colorCount);

   // Fill a small rectangle with each of the colors.
   SolidBrush* pSolidBrush;
   for(INT j = 0; j < colorCount; j++)
   {
      pSolidBrush = new SolidBrush(colors[j]);
      myGraphics.FillRectangle(pSolidBrush, 15*j, 0, 10, 10);
      delete(pSolidBrush);
   }
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>



<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-linear-gradient-use">Creating a Linear Gradient</a>



<a href="/windows/desktop/gdiplus/-gdiplus-filling-a-shape-with-a-color-gradient-use">Filling a Shape with a Color Gradient</a>



<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush">LinearGradientBrush</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-getinterpolationcolors">LinearGradientBrush::GetInterpolationColors</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-setinterpolationcolors">LinearGradientBrush::SetInterpolationColors</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>



<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush">SolidBrush</a>
