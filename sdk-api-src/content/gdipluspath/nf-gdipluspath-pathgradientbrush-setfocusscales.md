---
UID: NF:gdipluspath.PathGradientBrush.SetFocusScales
title: PathGradientBrush::SetFocusScales (gdipluspath.h)
description: The PathGradientBrush::SetFocusScales method sets the focus scales of this path gradient brush.
helpviewer_keywords: ["PathGradientBrush class [GDI+]","SetFocusScales method","PathGradientBrush.SetFocusScales","PathGradientBrush::SetFocusScales","SetFocusScales","SetFocusScales method [GDI+]","SetFocusScales method [GDI+]","PathGradientBrush class","_gdiplus_CLASS_PathGradientBrush_SetFocusScales_xScale_yScale_","gdiplus._gdiplus_CLASS_PathGradientBrush_SetFocusScales_xScale_yScale_"]
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_SetFocusScales_xScale_yScale_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushmethods\setfocusscales.htm
ms.date: 12/05/2018
ms.keywords: PathGradientBrush class [GDI+],SetFocusScales method, PathGradientBrush.SetFocusScales, PathGradientBrush::SetFocusScales, SetFocusScales, SetFocusScales method [GDI+], SetFocusScales method [GDI+],PathGradientBrush class, _gdiplus_CLASS_PathGradientBrush_SetFocusScales_xScale_yScale_, gdiplus._gdiplus_CLASS_PathGradientBrush_SetFocusScales_xScale_yScale_
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
 - PathGradientBrush::SetFocusScales
 - gdipluspath/PathGradientBrush::SetFocusScales
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
 - PathGradientBrush.SetFocusScales
---

# PathGradientBrush::SetFocusScales


## -description

The <b>PathGradientBrush::SetFocusScales</b> method sets the focus scales of this path gradient brush.

## -parameters

### -param xScale [in]

Type: <b>REAL</b>

Real number that specifies the x focus scale.

### -param yScale [in]

Type: <b>REAL</b>

Real number that specifies the y focus scale.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

By default, the center color of a path gradient is at the center point. By calling <b>PathGradientBrush::SetFocusScales</b>, you can specify that the center color should appear along a path that surrounds the center point. That path is the boundary path scaled by a factor of 
				<i>xScale</i> in the x direction and by a factor of 
				<i>yScale</i> in the y direction. The area inside the scaled path is filled with the center color.


#### Examples



The following example creates a 
						<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a> object based on a triangular path. The code calls the <b>PathGradientBrush::SetFocusScales</b> method of the 
						<b>PathGradientBrush</b> object to set the brush's focus scales to (0.2, 0.2). Then the code uses the path gradient brush to paint a rectangle that includes the triangular path.


```cpp
VOID Example_SetFocusScales(HDC hdc)
{
   Graphics graphics(hdc);

   Point points[] = {Point(100, 0), Point(200, 200), Point(0, 200)};

   // No GraphicsPath object is created. The PathGradientBrush
   // object is constructed directly from the array of points.
   PathGradientBrush pthGrBrush(points, 3);

   Color colors[] = {
      Color(255, 255, 0, 0),    // red
      Color(255, 0, 0, 255)};   // blue

   REAL relativePositions[] = {
      0.0f,    // red at the boundary of the outer triangle
      1.0f};   // blue at the boundary of the inner triangle

   pthGrBrush.SetInterpolationColors(colors, relativePositions, 2);

   // The inner triangle is formed by scaling the outer triangle
   // about its centroid. The scaling factor is 0.2 in both
   // the x and y directions.
   pthGrBrush.SetFocusScales(0.2f, 0.2f);

   // Fill a rectangle that is larger than the triangle
   // specified in the Point array. The portion of the
   // rectangle outside the triangle will not be painted.
   graphics.FillRectangle(&pthGrBrush, 0, 0, 200, 200); 
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="/windows/desktop/gdiplus/-gdiplus-filling-a-shape-with-a-color-gradient-use">Filling a Shape with a Color Gradient</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-getfocusscales">PathGradientBrush::GetFocusScales</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setinterpolationcolors">PathGradientBrush::SetInterpolationColors</a>