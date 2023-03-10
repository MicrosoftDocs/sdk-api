---
UID: NF:gdipluspath.PathGradientBrush.SetBlendTriangularShape
title: PathGradientBrush::SetBlendTriangularShape (gdipluspath.h)
description: The PathGradientBrush::SetBlendTriangularShape method sets the blend shape of this path gradient brush.
helpviewer_keywords: ["PathGradientBrush class [GDI+]","SetBlendTriangularShape method","PathGradientBrush.SetBlendTriangularShape","PathGradientBrush::SetBlendTriangularShape","SetBlendTriangularShape","SetBlendTriangularShape method [GDI+]","SetBlendTriangularShape method [GDI+]","PathGradientBrush class","_gdiplus_CLASS_PathGradientBrush_SetBlendTriangularShape_focus_scale_","gdiplus._gdiplus_CLASS_PathGradientBrush_SetBlendTriangularShape_focus_scale_"]
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_SetBlendTriangularShape_focus_scale_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushmethods\setblendtriangularshape_1focus_scale.htm
ms.date: 12/05/2018
ms.keywords: PathGradientBrush class [GDI+],SetBlendTriangularShape method, PathGradientBrush.SetBlendTriangularShape, PathGradientBrush::SetBlendTriangularShape, SetBlendTriangularShape, SetBlendTriangularShape method [GDI+], SetBlendTriangularShape method [GDI+],PathGradientBrush class, _gdiplus_CLASS_PathGradientBrush_SetBlendTriangularShape_focus_scale_, gdiplus._gdiplus_CLASS_PathGradientBrush_SetBlendTriangularShape_focus_scale_
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
 - PathGradientBrush::SetBlendTriangularShape
 - gdipluspath/PathGradientBrush::SetBlendTriangularShape
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
 - PathGradientBrush.SetBlendTriangularShape
---

# PathGradientBrush::SetBlendTriangularShape


## -description

The <b>PathGradientBrush::SetBlendTriangularShape</b> method sets the blend shape of this path gradient brush.

## -parameters

### -param focus [in]

Type: <b>REAL</b>

Real number that specifies where the center color will be at its highest intensity. This number must be in the range 0 through 1.

### -param scale [in, optional]

Type: <b>REAL</b>

Optional. Real number that specifies the maximum intensity of center color that gets blended with the boundary color. This number must be in the range 0 through 1. The default value is 1.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

By default, as you move from the boundary of a path gradient to the center point, the color changes gradually from the boundary color to the center color. You can customize the positioning and blending of the boundary and center colors by calling the <b>PathGradientBrush::SetBlendTriangularShape</b> method.


#### Examples



The following example creates a 
						<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a> object based on an ellipse. The code calls the <b>PathGradientBrush::SetBlendTriangularShape</b> method of the 
						<b>PathGradientBrush</b> object, passing a focus of 0.2 and a scale of 0.7. Then the code uses the path gradient brush to paint a rectangle that contains the ellipse.


```cpp
VOID Example_SetBlendShape(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a path that consists of a single ellipse.
   GraphicsPath path;
   path.AddEllipse(0, 0, 200, 100);

   // Use the path to construct a brush.
   PathGradientBrush pthGrBrush(&path);

   // Set the color at the center of the path to red.
   pthGrBrush.SetCenterColor(Color(255, 255, 0, 0));

   // Set the color along the entire boundary of the path to blue.
   Color colors[] = {Color(255, 0, 0, 255)};
   INT count = 1;
   pthGrBrush.SetSurroundColors(colors, &count);

   pthGrBrush.SetBlendTriangularShape(0.2f, 0.7f);

   // The color is blue on the boundary and at the center.
   // At points that are 20 percent of the way from the boundary to the
   // center, the color is 70 percent red and 30 percent blue.

   graphics.FillRectangle(&pthGrBrush, 0, 0, 300, 300); 
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>



<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="/windows/desktop/gdiplus/-gdiplus-filling-a-shape-with-a-color-gradient-use">Filling a Shape with a Color Gradient</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-getblend">PathGradientBrush::GetBlend</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-getblendcount">PathGradientBrush::GetBlendCount</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setblend">PathGradientBrush::SetBlend</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setblendbellshape">PathGradientBrush::SetBlendBellShape</a>