---
UID: NF:gdipluspath.PathGradientBrush.GetWrapMode
title: PathGradientBrush::GetWrapMode (gdipluspath.h)
description: The PathGradientBrush::GetWrapMode method gets the wrap mode currently set for this path gradient brush.
helpviewer_keywords: ["GetWrapMode","GetWrapMode method [GDI+]","GetWrapMode method [GDI+]","PathGradientBrush class","PathGradientBrush class [GDI+]","GetWrapMode method","PathGradientBrush.GetWrapMode","PathGradientBrush::GetWrapMode","_gdiplus_CLASS_PathGradientBrush_GetWrapMode_","gdiplus._gdiplus_CLASS_PathGradientBrush_GetWrapMode_"]
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_GetWrapMode_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushmethods\getwrapmode_45.htm
ms.date: 12/05/2018
ms.keywords: GetWrapMode, GetWrapMode method [GDI+], GetWrapMode method [GDI+],PathGradientBrush class, PathGradientBrush class [GDI+],GetWrapMode method, PathGradientBrush.GetWrapMode, PathGradientBrush::GetWrapMode, _gdiplus_CLASS_PathGradientBrush_GetWrapMode_, gdiplus._gdiplus_CLASS_PathGradientBrush_GetWrapMode_
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
 - PathGradientBrush::GetWrapMode
 - gdipluspath/PathGradientBrush::GetWrapMode
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
 - PathGradientBrush.GetWrapMode
---

# PathGradientBrush::GetWrapMode


## -description

The <b>PathGradientBrush::GetWrapMode</b> method gets the wrap mode currently set for this path gradient brush.



## -returns

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-wrapmode">WrapMode</a></b>

This method returns an element of the 
						<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-wrapmode">WrapMode</a> enumeration that indicates the wrap mode currently set for this path gradient brush.

## -remarks

The bounding rectangle of a path gradient brush is the smallest rectangle that encloses the brush's boundary path. When you paint the bounding rectangle with the path gradient brush, only the area inside the boundary path gets filled. The area inside the bounding rectangle but outside the boundary path does not get filled.

The default wrap mode for a path gradient brush is WrapModeClamp, which indicates that no painting occurs outside of the brush's bounding rectangle. All of the other wrap modes indicate that areas outside the brush's bounding rectangle will be tiled. Each tile is a copy (possibly flipped) of the filled path inside its bounding rectangle.


#### Examples



The following example creates a 
						<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a> object based on a triangular path. The code calls the <a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setwrapmode">PathGradientBrush::SetWrapMode</a> method of the 
						<b>PathGradientBrush</b> object to set the wrap mode to <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-wrapmode">WrapModeTileFlipX</a>. Next, the code calls the <b>PathGradientBrush::GetWrapMode</b> method of the 
						<b>PathGradientBrush</b> object to obtain the brush's wrap mode. If the obtained wrap mode is WrapModeTileFlipX, the code calls 
						<a href="/previous-versions/ms535957(v=vs.85)">FillRectangle</a> to tile a large area with the path gradient brush. 


```cpp
VOID Example_GetWrapMode(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a path gradient brush based on an array of points,
   // and set its wrap mode.
   Point points[] = {
      Point(0, 0), 
      Point(100, 0), 
      Point(100, 100)};

   Color colors[] = {
      Color(255, 255, 0, 0),   // red
      Color(255, 0, 0, 255),   // blue
      Color(255, 0, 255, 0)};  // green

   INT count = 3;

   PathGradientBrush pthGrBrush(points, 3);
   pthGrBrush.SetSurroundColors(colors, &count);
   pthGrBrush.SetWrapMode(WrapModeTileFlipX);

   // Obtain information about the path gradient brush.
   WrapMode wrapMode; 
   wrapMode = pthGrBrush.GetWrapMode();

   if(wrapMode == WrapModeTileFlipX)
         graphics.FillRectangle(&pthGrBrush, 0, 0, 800, 800);
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="/windows/desktop/gdiplus/-gdiplus-filling-a-shape-with-a-color-gradient-use">Filling a Shape with a Color Gradient</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setwrapmode">PathGradientBrush::SetWrapMode</a>



<a href="/windows/desktop/gdiplus/-gdiplus-tiling-a-shape-with-an-image-use">Tiling a Shape with an Image</a>
