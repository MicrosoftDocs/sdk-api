---
UID: NF:gdiplusbrush.LinearGradientBrush.SetBlendTriangularShape
title: LinearGradientBrush::SetBlendTriangularShape (gdiplusbrush.h)
description: The LinearGradientBrush::SetBlendTriangularShape method sets the blend shape of this linear gradient brush to create a custom blend based on a triangular shape.
helpviewer_keywords: ["LinearGradientBrush class [GDI+]","SetBlendTriangularShape method","LinearGradientBrush.SetBlendTriangularShape","LinearGradientBrush::SetBlendTriangularShape","SetBlendTriangularShape","SetBlendTriangularShape method [GDI+]","SetBlendTriangularShape method [GDI+]","LinearGradientBrush class","_gdiplus_CLASS_LinearGradientBrush_SetBlendTriangularShape_focus_scale_","gdiplus._gdiplus_CLASS_LinearGradientBrush_SetBlendTriangularShape_focus_scale_"]
old-location: gdiplus\_gdiplus_CLASS_LinearGradientBrush_SetBlendTriangularShape_focus_scale_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\lineargradientbrushclass\lineargradientbrushmethods\setblendtriangularshape.htm
ms.date: 12/05/2018
ms.keywords: LinearGradientBrush class [GDI+],SetBlendTriangularShape method, LinearGradientBrush.SetBlendTriangularShape, LinearGradientBrush::SetBlendTriangularShape, SetBlendTriangularShape, SetBlendTriangularShape method [GDI+], SetBlendTriangularShape method [GDI+],LinearGradientBrush class, _gdiplus_CLASS_LinearGradientBrush_SetBlendTriangularShape_focus_scale_, gdiplus._gdiplus_CLASS_LinearGradientBrush_SetBlendTriangularShape_focus_scale_
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
 - LinearGradientBrush::SetBlendTriangularShape
 - gdiplusbrush/LinearGradientBrush::SetBlendTriangularShape
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
 - LinearGradientBrush.SetBlendTriangularShape
---

# LinearGradientBrush::SetBlendTriangularShape


## -description

The <b>LinearGradientBrush::SetBlendTriangularShape</b> method sets the blend shape of this linear gradient brush to create a custom blend based on a triangular shape.

## -parameters

### -param focus [in]

Type: <b>REAL</b>

Real number that specifies the position of the ending color. This number is a percentage of the distance between the boundary lines and must be in the range from 0.0 through 1.0.

### -param scale [in]

Type: <b>REAL</b>

Optional. Real number that specifies the percentage of the gradient's ending color that gets blended, at the focus position, with the gradient's starting color. This number must be in the range from 0.0 through 1.0. The default value is 1.0, which specifies that the ending color is at full intensity.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

By default, the color changes gradually from the starting color (color at the starting boundary of the linear gradient brush) to the ending color (color at the ending boundary of the linear gradient brush) as you move from the starting boundary to the ending boundary. You can customize the positioning and blending of the starting and ending colors by using the <b>LinearGradientBrush::SetBlendTriangularShape</b> method.

The <b>LinearGradientBrush::SetBlendTriangularShape</b> method customizes the blend so that it follows a triangular shape with the extremes of the triangle's base at the gradient's boundaries. The starting color, which, in a default blend, is at the starting boundary of a linear gradient brush, appears at the starting and ending boundaries of the linear gradient brush when a triangular-shaped blend is applied. The position of the ending color, which, in a default blend, is at the ending boundary, is somewhere between the boundaries and is determined by the value of the focus. In other words, the focus specifies the position of the peak of the triangle. For example, a focus value of 0.5 places the peak half way between the starting and ending boundaries. The ending color appears at this peak.

The ending color in a triangular-shaped blend is a percentage of the gamut between the gradient's default-blend starting color and default-blend ending color. For example, suppose a linear gradient brush is constructed with red as the starting color and blue as the ending color. If <b>LinearGradientBrush::SetBlendTriangularShape</b> is called with a scale value of 0.3, the ending color in the triangular-shaped blend is a hue that is 30 percent between red and blue (70 percent red, 30 percent blue). A scale value of 1.0 produces an ending color that is 100 percent blue.


#### Examples



The following example creates a linear gradient brush, sets a triangular-shaped blend, and uses the brush to fill a rectangle. Twice more, the code sets a triangular-shaped blend with different values and, each time, uses the brush to fill a rectangle.


```cpp
VOID Example_SetBlendTri(HDC hdc)
{
   Graphics myGraphics(hdc);

   LinearGradientBrush linGrBrush(
      Point(0, 0),
      Point(500, 0),
      Color(255, 255, 0, 0),   // red
      Color(255, 0, 0, 255));  // blue

   linGrBrush.SetBlendTriangularShape(0.5f, 0.6f);
   myGraphics.FillRectangle(&linGrBrush, 0, 0, 500, 50);

   linGrBrush.SetBlendTriangularShape(0.5f, 0.8f); 
   myGraphics.FillRectangle(&linGrBrush, 0, 75, 500, 50);

   linGrBrush.SetBlendTriangularShape(0.5f, 1.0f); 
   myGraphics.FillRectangle(&linGrBrush, 0, 150, 500, 50);
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-linear-gradient-use">Creating a Linear Gradient</a>



<a href="/windows/desktop/gdiplus/-gdiplus-filling-a-shape-with-a-color-gradient-use">Filling a Shape with a Color Gradient</a>



<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush">LinearGradientBrush</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-getblend">LinearGradientBrush::GetBlend</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-setblend">LinearGradientBrush::SetBlend</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-setblendbellshape">LinearGradientBrush::SetBlendBellShape</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>