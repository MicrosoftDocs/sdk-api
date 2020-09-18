---
UID: NF:gdiplusbrush.LinearGradientBrush.SetInterpolationColors
title: LinearGradientBrush::SetInterpolationColors (gdiplusbrush.h)
description: The LinearGradientBrush::SetInterpolationColors method sets the colors to be interpolated for this linear gradient brush and their corresponding blend positions.
helpviewer_keywords: ["LinearGradientBrush class [GDI+]","SetInterpolationColors method","LinearGradientBrush.SetInterpolationColors","LinearGradientBrush::SetInterpolationColors","SetInterpolationColors","SetInterpolationColors method [GDI+]","SetInterpolationColors method [GDI+]","LinearGradientBrush class","_gdiplus_CLASS_LinearGradientBrush_SetInterpolationColors_presetColors_blendPositions_count_","gdiplus._gdiplus_CLASS_LinearGradientBrush_SetInterpolationColors_presetColors_blendPositions_count_"]
old-location: gdiplus\_gdiplus_CLASS_LinearGradientBrush_SetInterpolationColors_presetColors_blendPositions_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\lineargradientbrushclass\lineargradientbrushmethods\setinterpolationcolors.htm
ms.date: 12/05/2018
ms.keywords: LinearGradientBrush class [GDI+],SetInterpolationColors method, LinearGradientBrush.SetInterpolationColors, LinearGradientBrush::SetInterpolationColors, SetInterpolationColors, SetInterpolationColors method [GDI+], SetInterpolationColors method [GDI+],LinearGradientBrush class, _gdiplus_CLASS_LinearGradientBrush_SetInterpolationColors_presetColors_blendPositions_count_, gdiplus._gdiplus_CLASS_LinearGradientBrush_SetInterpolationColors_presetColors_blendPositions_count_
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
 - LinearGradientBrush::SetInterpolationColors
 - gdiplusbrush/LinearGradientBrush::SetInterpolationColors
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
 - LinearGradientBrush.SetInterpolationColors
---

# LinearGradientBrush::SetInterpolationColors


## -description

The <b>LinearGradientBrush::SetInterpolationColors</b> method sets the colors to be interpolated for this linear gradient brush and their corresponding blend positions.

## -parameters

### -param presetColors [in]

Type: <b>const <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>*</b>

Pointer to an array of <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a> objects that specify the colors to be interpolated for this linear gradient brush. A color of a given index in the 
					<i>presetColors</i> array corresponds to the blend position of that same index in the 
					<i>blendPositions</i> array.

### -param blendPositions [in]

Type: <b>const REAL*</b>

Pointer to an array of real numbers that specify the blend positions. Each number in the array specifies a percentage of the distance between the starting boundary and the ending boundary and is in the range from 0.0 through 1.0, where 0.0 indicates the starting boundary of the gradient and 1.0 indicates the ending boundary. There must be at least two positions specified: the first position, which is always 0.0f, and the last position, which is always 1.0f. Otherwise, the behavior is undefined. A blend position between 0.0 and 1.0 indicates the line, parallel to the boundary lines, that is a certain fraction of the distance from the starting boundary to the ending boundary. For example, a blend position of 0.7 indicates the line that is 70 percent of the distance from the starting boundary to the ending boundary. The color is constant on lines that are parallel to the boundary lines.

### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the 
					<i>presetColors</i> array. This is the same as the number of elements in the 
					<i>blendPositions</i> array.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>



<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-linear-gradient-use">Creating a Linear Gradient</a>



<a href="/windows/desktop/gdiplus/-gdiplus-filling-a-shape-with-a-color-gradient-use">Filling a Shape with a Color Gradient</a>



<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush">LinearGradientBrush</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-getinterpolationcolors">LinearGradientBrush::GetInterpolationColors</a>