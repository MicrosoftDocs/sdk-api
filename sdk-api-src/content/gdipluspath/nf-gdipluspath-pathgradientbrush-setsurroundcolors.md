---
UID: NF:gdipluspath.PathGradientBrush.SetSurroundColors
title: PathGradientBrush::SetSurroundColors (gdipluspath.h)
description: The PathGradientBrush::SetSurroundColors method sets the surround colors of this path gradient brush. The surround colors are colors specified for discrete points on the brush's boundary path.
helpviewer_keywords: ["PathGradientBrush class [GDI+]","SetSurroundColors method","PathGradientBrush.SetSurroundColors","PathGradientBrush::SetSurroundColors","SetSurroundColors","SetSurroundColors method [GDI+]","SetSurroundColors method [GDI+]","PathGradientBrush class","_gdiplus_CLASS_PathGradientBrush_SetSurroundColors_colors_count_","gdiplus._gdiplus_CLASS_PathGradientBrush_SetSurroundColors_colors_count_"]
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_SetSurroundColors_colors_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushmethods\setsurroundcolors.htm
ms.date: 12/05/2018
ms.keywords: PathGradientBrush class [GDI+],SetSurroundColors method, PathGradientBrush.SetSurroundColors, PathGradientBrush::SetSurroundColors, SetSurroundColors, SetSurroundColors method [GDI+], SetSurroundColors method [GDI+],PathGradientBrush class, _gdiplus_CLASS_PathGradientBrush_SetSurroundColors_colors_count_, gdiplus._gdiplus_CLASS_PathGradientBrush_SetSurroundColors_colors_count_
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
 - PathGradientBrush::SetSurroundColors
 - gdipluspath/PathGradientBrush::SetSurroundColors
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
 - PathGradientBrush.SetSurroundColors
---

# PathGradientBrush::SetSurroundColors


## -description

The <b>PathGradientBrush::SetSurroundColors</b> method sets the surround colors of this path gradient brush. The surround colors are colors specified for discrete points on the brush's boundary path.

## -parameters

### -param colors [in]

Type: <b>const <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>*</b>

Pointer to an array of <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a> objects that specify the surround colors.

### -param count [in, out]

Type: <b>INT*</b>

Pointer to an integer that, on input, specifies the number of <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a> objects in the 
					<i>colors</i> array. If the method succeeds, this parameter, on output, receives the number of surround colors set. If the method fails, this parameter does not receive a value.

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
						<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a> object based on an array of three points that defines a triangular path. The code also initializes an array of three <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a> objects. The call to the <b>PathGradientBrush::SetSurroundColors</b> method associates each color in the color array with the corresponding (same index) point in the point array. After the surround colors of the path gradient brush have been set, the 
						<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inconstrect_)">Graphics::FillRectangle</a> method uses the path gradient brush to paint a rectangle that includes the triangular path.

One edge of the rendered triangle changes gradually from red to green. The next edge changes gradually from green to black, and the third edge changes gradually from black to red. The code does not set the center color, so the center color has the default value of black. As you move along a straight line from any point on the boundary path (triangle) to the center point, the color changes gradually from that boundary point's color to black.


```cpp
VOID Example_SetSurColor(HDC hdc)
{
   Graphics graphics(hdc);

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
   
   graphics.FillRectangle(&pthGrBrush, 0, 0, 200, 200);
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>



<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="/windows/desktop/gdiplus/-gdiplus-filling-a-shape-with-a-color-gradient-use">Filling a Shape with a Color Gradient</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-getsurroundcolorcount">PathGradientBrush::GetSurroundColorCount</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-getsurroundcolors">PathGradientBrush::GetSurroundColors</a>