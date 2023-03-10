---
UID: NF:gdiplusbrush.LinearGradientBrush.SetBlendBellShape
title: LinearGradientBrush::SetBlendBellShape (gdiplusbrush.h)
description: The LinearGradientBrush::SetBlendBellShape method sets the blend shape of this linear gradient brush to create a custom blend based on a bell-shaped curve.
helpviewer_keywords: ["LinearGradientBrush class [GDI+]","SetBlendBellShape method","LinearGradientBrush.SetBlendBellShape","LinearGradientBrush::SetBlendBellShape","SetBlendBellShape","SetBlendBellShape method [GDI+]","SetBlendBellShape method [GDI+]","LinearGradientBrush class","_gdiplus_CLASS_LinearGradientBrush_SetBlendBellShape_focus_scale_","gdiplus._gdiplus_CLASS_LinearGradientBrush_SetBlendBellShape_focus_scale_"]
old-location: gdiplus\_gdiplus_CLASS_LinearGradientBrush_SetBlendBellShape_focus_scale_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\lineargradientbrushclass\lineargradientbrushmethods\setblendbellshape.htm
ms.date: 12/05/2018
ms.keywords: LinearGradientBrush class [GDI+],SetBlendBellShape method, LinearGradientBrush.SetBlendBellShape, LinearGradientBrush::SetBlendBellShape, SetBlendBellShape, SetBlendBellShape method [GDI+], SetBlendBellShape method [GDI+],LinearGradientBrush class, _gdiplus_CLASS_LinearGradientBrush_SetBlendBellShape_focus_scale_, gdiplus._gdiplus_CLASS_LinearGradientBrush_SetBlendBellShape_focus_scale_
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
 - LinearGradientBrush::SetBlendBellShape
 - gdiplusbrush/LinearGradientBrush::SetBlendBellShape
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
 - LinearGradientBrush.SetBlendBellShape
---

# LinearGradientBrush::SetBlendBellShape


## -description

The <b>LinearGradientBrush::SetBlendBellShape</b> method sets the blend shape of this linear gradient brush to create a custom blend based on a bell-shaped curve.

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

By default, the color changes gradually from the starting color (color at the starting boundary of the linear gradient brush) to the ending color (color at the ending boundary of the linear gradient brush) as you move from the starting boundary to the ending boundary. You can customize the positioning and blending of the starting and ending colors by using the <b>LinearGradientBrush::SetBlendBellShape</b> method.

The <b>LinearGradientBrush::SetBlendBellShape</b> method customizes the blend so that it follows a bell-shaped curve with the extremes of the bell's base at the gradient's boundaries. The starting color, which, in a default blend, is at the starting boundary of a linear gradient brush, appears at the starting and ending boundaries of the linear gradient brush when a bell-shaped blend is applied. The position of the ending color, which, in a default blend, is at the ending boundary, is somewhere between the boundaries and is determined by the value of the focus. In other words, the focus specifies the position of the peak of the bell. For example, a focus value of 0.7 places the peak at 70 percent of the distance between the starting and ending boundaries. The ending color appears at this peak.

The ending color in a bell-shaped blend is a percentage of the gamut between the gradient's default-blend starting color and default-blend ending color. For example, suppose a linear gradient brush is constructed with red as the starting color and blue as the ending color. If <b>LinearGradientBrush::SetBlendBellShape</b> is called with a scale value of 0.8, the ending color in the bell shaped blend is a hue that is 80 percent between red and blue (20 percent red, 80 percent blue). A scale value of 1.0 produces an ending color that is 100 percent blue.


#### Examples



The following example creates a linear gradient brush, sets a bell-shaped blend, and uses the brush to fill a rectangle. Twice more, the code sets a bell-shaped blend with different values and, each time, uses the brush to fill a rectangle.


```cpp
VOID Example_SetBlendBell(HDC hdc)
{
   Graphics myGraphics(hdc);

   LinearGradientBrush linGrBrush(
      Point(0, 0),
      Point(500, 0),
      Color(255, 255, 0, 0),   // red
      Color(255, 0, 0, 255));  // blue

   linGrBrush.SetBlendBellShape(0.5f, 0.6f);
   myGraphics.FillRectangle(&linGrBrush, 0, 0, 500, 50);

   linGrBrush.SetBlendBellShape(0.5f, 0.8f); 
   myGraphics.FillRectangle(&linGrBrush, 0, 75, 500, 50);

   linGrBrush.SetBlendBellShape(0.5f, 1.0f); 
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



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-setblendtriangularshape">LinearGradientBrush::SetBlendTriangularShape</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-a-brush-to-fill-shapes-use">Using a Brush to Fill Shapes</a>