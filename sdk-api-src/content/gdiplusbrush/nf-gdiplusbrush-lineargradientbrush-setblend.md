---
UID: NF:gdiplusbrush.LinearGradientBrush.SetBlend
title: LinearGradientBrush::SetBlend (gdiplusbrush.h)
description: The LinearGradientBrush::SetBlend method sets the blend factors and the blend positions of this linear gradient brush to create a custom blend.
helpviewer_keywords: ["LinearGradientBrush class [GDI+]","SetBlend method","LinearGradientBrush.SetBlend","LinearGradientBrush::SetBlend","SetBlend","SetBlend method [GDI+]","SetBlend method [GDI+]","LinearGradientBrush class","_gdiplus_CLASS_LinearGradientBrush_SetBlend_blendFactors_blendPositions_count_","gdiplus._gdiplus_CLASS_LinearGradientBrush_SetBlend_blendFactors_blendPositions_count_"]
old-location: gdiplus\_gdiplus_CLASS_LinearGradientBrush_SetBlend_blendFactors_blendPositions_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\lineargradientbrushclass\lineargradientbrushmethods\setblend.htm
ms.date: 12/05/2018
ms.keywords: LinearGradientBrush class [GDI+],SetBlend method, LinearGradientBrush.SetBlend, LinearGradientBrush::SetBlend, SetBlend, SetBlend method [GDI+], SetBlend method [GDI+],LinearGradientBrush class, _gdiplus_CLASS_LinearGradientBrush_SetBlend_blendFactors_blendPositions_count_, gdiplus._gdiplus_CLASS_LinearGradientBrush_SetBlend_blendFactors_blendPositions_count_
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
 - LinearGradientBrush::SetBlend
 - gdiplusbrush/LinearGradientBrush::SetBlend
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
 - LinearGradientBrush.SetBlend
---

# LinearGradientBrush::SetBlend


## -description

The <b>LinearGradientBrush::SetBlend</b> method sets the blend factors and the blend positions of this linear gradient brush to create a custom blend.

## -parameters

### -param blendFactors [in]

Type: <b>const REAL*</b>

Pointer to an array of real numbers that specify blend factors. Each number in the array specifies a percentage of the ending color and should be in the range from 0.0 through 1.0.

### -param blendPositions [in]

Type: <b>const REAL*</b>

Pointer to an array of real numbers that specify blend positions. Each number in the array indicates a percentage of the distance between the starting boundary and the ending boundary and is in the range from 0.0 through 1.0, where 0.0 indicates the starting boundary of the gradient and 1.0 indicates the ending boundary. There must be at least two positions specified: the first position, which is always 0.0f, and the last position, which is always 1.0f. Otherwise, the behavior is undefined. A blend position between 0.0 and 1.0 indicates a line, parallel to the boundary lines, that is a certain fraction of the distance from the starting boundary to the ending boundary. For example, a blend position of 0.7 indicates the line that is 70 percent of the distance from the starting boundary to the ending boundary. The color is constant on lines that are parallel to the boundary lines.

### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the 
					<i>blendFactors</i> array. This is the same as the number of elements in the 
					<i>blendPositions</i> array. The blend factor at a given array index corresponds to the blend position at that same array index.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

A 
				<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush">LinearGradientBrush</a> object has two boundaries. When you fill an area with a linear gradient brush, the color changes gradually as you move from the starting boundary to the ending boundary. By default, the color is linearly related to the distance, but you can customize the relationship between color and distance by calling the <b>LinearGradientBrush::SetBlend</b> method.


#### Examples



The following example creates a linear gradient brush, sets a custom blend, and uses the brush to fill a rectangle.


```cpp
VOID Example_SetBlend(HDC hdc)
{
   Graphics myGraphics(hdc);

   REAL factors[4] = {0.0f, 0.4f, 0.6f, 1.0f};
   REAL positions[4] = {0.0f, 0.2f, 0.8f, 1.0f};
   Rect rect(0, 0, 100, 50);

   LinearGradientBrush linGrBrush(
      rect,
      Color(255, 255, 0, 0),  // red
      Color(255, 0, 0, 255),  // blue
      LinearGradientModeHorizontal);

   linGrBrush.SetBlend(factors, positions, 4);
   myGraphics.FillRectangle(&linGrBrush, rect);
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>



<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-linear-gradient-use">Creating a Linear Gradient</a>



<a href="/windows/desktop/gdiplus/-gdiplus-filling-a-shape-with-a-color-gradient-use">Filling a Shape with a Color Gradient</a>



<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush">LinearGradientBrush</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-getblend">LinearGradientBrush::GetBlend</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>