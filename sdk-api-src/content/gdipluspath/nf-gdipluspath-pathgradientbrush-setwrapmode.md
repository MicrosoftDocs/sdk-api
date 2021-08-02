---
UID: NF:gdipluspath.PathGradientBrush.SetWrapMode
title: PathGradientBrush::SetWrapMode (gdipluspath.h)
description: The PathGradientBrush::SetWrapMode method sets the wrap mode of this path gradient brush.
helpviewer_keywords: ["PathGradientBrush class [GDI+]","SetWrapMode method","PathGradientBrush.SetWrapMode","PathGradientBrush::SetWrapMode","SetWrapMode","SetWrapMode method [GDI+]","SetWrapMode method [GDI+]","PathGradientBrush class","_gdiplus_CLASS_PathGradientBrush_SetWrapMode_wrapMode_","gdiplus._gdiplus_CLASS_PathGradientBrush_SetWrapMode_wrapMode_"]
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_SetWrapMode_wrapMode_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushmethods\setwrapmode_12wrapmode.htm
ms.date: 12/05/2018
ms.keywords: PathGradientBrush class [GDI+],SetWrapMode method, PathGradientBrush.SetWrapMode, PathGradientBrush::SetWrapMode, SetWrapMode, SetWrapMode method [GDI+], SetWrapMode method [GDI+],PathGradientBrush class, _gdiplus_CLASS_PathGradientBrush_SetWrapMode_wrapMode_, gdiplus._gdiplus_CLASS_PathGradientBrush_SetWrapMode_wrapMode_
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
 - PathGradientBrush::SetWrapMode
 - gdipluspath/PathGradientBrush::SetWrapMode
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
 - PathGradientBrush.SetWrapMode
---

# PathGradientBrush::SetWrapMode


## -description

The <b>PathGradientBrush::SetWrapMode</b> method sets the wrap mode of this path gradient brush.

## -parameters

### -param wrapMode [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-wrapmode">WrapMode</a></b>

Element of the 
					<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-wrapmode">WrapMode</a> enumeration that specifies how areas painted with the path gradient brush will be tiled. The default value is <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-wrapmode">WrapModeClamp</a>.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

The bounding rectangle of a path gradient brush is the smallest rectangle that encloses the brush's boundary path. When you paint the bounding rectangle with the path gradient brush, only the area inside the boundary path gets filled. The area inside the bounding rectangle but outside the boundary path does not get filled.


<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-wrapmode">WrapModeClamp</a> (the default wrap mode) indicates that no painting occurs outside of the brush's bounding rectangle. All of the other wrap modes indicate that areas outside the brush's bounding rectangle will be tiled. Each tile is a copy (possibly flipped) of the filled path inside its bounding rectangle.


#### Examples



The following example creates a 
						<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a> object based on a triangular path. The code calls the <b>PathGradientBrush::SetWrapMode</b> method of the 
						<b>PathGradientBrush</b> object to set the brush's wrap mode to <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-wrapmode">WrapModeTileFlipX</a>. The 
						<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inconstrect_)">Graphics::FillRectangle</a> method uses the path gradient brush to tile a large area. 

The output of the code is a grid of tiles. As you move from one tile to the next in a given row, the image (filled boundary path inside the bounding rectangle) is flipped horizontally.


```cpp
VOID Example_SetWrapMode(HDC hdc)
{
   Graphics graphics(hdc);

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

   graphics.FillRectangle(&pthGrBrush, 0, 0, 800, 800); 
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="/windows/desktop/gdiplus/-gdiplus-filling-a-shape-with-a-color-gradient-use">Filling a Shape with a Color Gradient</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-getwrapmode">PathGradientBrush::GetWrapMode</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setwrapmode">PathGradientBrush::SetWrapMode</a>