---
UID: NF:gdipluspath.PathGradientBrush.GetSurroundColors
title: PathGradientBrush::GetSurroundColors (gdipluspath.h)
description: The PathGradientBrush::GetSurroundColors method gets the surround colors currently specified for this path gradient brush.
helpviewer_keywords: ["GetSurroundColors","GetSurroundColors method [GDI+]","GetSurroundColors method [GDI+]","PathGradientBrush class","PathGradientBrush class [GDI+]","GetSurroundColors method","PathGradientBrush.GetSurroundColors","PathGradientBrush::GetSurroundColors","_gdiplus_CLASS_PathGradientBrush_GetSurroundColors_colors_count_","gdiplus._gdiplus_CLASS_PathGradientBrush_GetSurroundColors_colors_count_"]
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_GetSurroundColors_colors_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushmethods\getsurroundcolors.htm
ms.date: 12/05/2018
ms.keywords: GetSurroundColors, GetSurroundColors method [GDI+], GetSurroundColors method [GDI+],PathGradientBrush class, PathGradientBrush class [GDI+],GetSurroundColors method, PathGradientBrush.GetSurroundColors, PathGradientBrush::GetSurroundColors, _gdiplus_CLASS_PathGradientBrush_GetSurroundColors_colors_count_, gdiplus._gdiplus_CLASS_PathGradientBrush_GetSurroundColors_colors_count_
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
 - PathGradientBrush::GetSurroundColors
 - gdipluspath/PathGradientBrush::GetSurroundColors
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
 - PathGradientBrush.GetSurroundColors
---

# PathGradientBrush::GetSurroundColors


## -description

The <b>PathGradientBrush::GetSurroundColors</b> method gets the surround colors currently specified for this path gradient brush.

## -parameters

### -param colors [in]

Type: <b><a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>*</b>

Pointer to an array that receives the surround colors.

### -param count [in, out]

Type: <b>INT*</b>

Pointer to an integer that, on input, specifies the number of colors requested. If the method succeeds, this parameter, on output, receives the number of colors retrieved. If the method fails, this parameter does not receive a value.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

A path gradient brush has a boundary path and a center point. The center point is set to a single color, but you can specify different colors for several points on the boundary. For example, suppose you specify red for the center color, and you specify blue, green, and yellow for distinct points on the boundary. Then as you move along the boundary, the color will change gradually from blue to green to yellow and back to blue. As you move along a straight line from any point on the boundary to the center point, the color will change from that boundary point's color to red.


#### Examples



The following example creates a 
						<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a> object based on a triangular path that is defined by an array of three points. The code calls the <a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setsurroundcolors">PathGradientBrush::SetSurroundColors</a> method of the 
						<b>PathGradientBrush</b> object to specify a color for each of the points that define the triangle. The <a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-getsurroundcolorcount">PathGradientBrush::GetSurroundColorCount</a> method determines the current number of surround colors (the colors specified for the brush's boundary path). Next, the code allocates a buffer large enough to receive the array of surround colors and calls <b>PathGradientBrush::GetSurroundColors</b> to fill that buffer. Finally the code fills a small square with each of the brush's surround colors.


```cpp
VOID Example_GetSurColors(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a path gradient brush and set its surround colors.
   Point pts[] = {
      Point(20, 20), 
      Point(100, 20), 
      Point(100, 100)};

   Color cols[] = {
      Color(255, 255, 0, 0),  // red
      Color(255, 0, 255, 0),  // green
      Color(255, 0, 0, 0)};   // black

   INT count = 3;
   PathGradientBrush pthGrBrush(pts, 3);
   pthGrBrush.SetSurroundColors(cols, &count);
   
   // Obtain information about the path gradient brush.
   INT colorCount = pthGrBrush.GetSurroundColorCount();
   Color* colors = new Color[colorCount];
   pthGrBrush.GetSurroundColors(colors, &colorCount);

   // Fill a small square with each of the surround colors.
   SolidBrush solidBrush(Color(255, 255, 255, 255));

   for(INT j = 0; j < colorCount; ++j)
   {
      solidBrush.SetColor(colors[j]);
      graphics.FillRectangle(&solidBrush, 15*j, 0, 10, 10);
   }

   delete [] colors;
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>



<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="/windows/desktop/gdiplus/-gdiplus-filling-a-shape-with-a-color-gradient-use">Filling a Shape with a Color Gradient</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-getsurroundcolorcount">PathGradientBrush::GetSurroundColorCount</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setsurroundcolors">PathGradientBrush::SetSurroundColors</a>