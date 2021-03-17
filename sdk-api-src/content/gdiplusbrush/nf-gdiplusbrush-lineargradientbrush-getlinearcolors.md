---
UID: NF:gdiplusbrush.LinearGradientBrush.GetLinearColors
title: LinearGradientBrush::GetLinearColors (gdiplusbrush.h)
description: The LinearGradientBrush::GetLinearColors method gets the starting color and ending color of this linear gradient brush.
helpviewer_keywords: ["GetLinearColors","GetLinearColors method [GDI+]","GetLinearColors method [GDI+]","LinearGradientBrush class","LinearGradientBrush class [GDI+]","GetLinearColors method","LinearGradientBrush.GetLinearColors","LinearGradientBrush::GetLinearColors","_gdiplus_CLASS_LinearGradientBrush_GetLinearColors_colors_","gdiplus._gdiplus_CLASS_LinearGradientBrush_GetLinearColors_colors_"]
old-location: gdiplus\_gdiplus_CLASS_LinearGradientBrush_GetLinearColors_colors_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\lineargradientbrushclass\lineargradientbrushmethods\getlinearcolors.htm
ms.date: 12/05/2018
ms.keywords: GetLinearColors, GetLinearColors method [GDI+], GetLinearColors method [GDI+],LinearGradientBrush class, LinearGradientBrush class [GDI+],GetLinearColors method, LinearGradientBrush.GetLinearColors, LinearGradientBrush::GetLinearColors, _gdiplus_CLASS_LinearGradientBrush_GetLinearColors_colors_, gdiplus._gdiplus_CLASS_LinearGradientBrush_GetLinearColors_colors_
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
 - LinearGradientBrush::GetLinearColors
 - gdiplusbrush/LinearGradientBrush::GetLinearColors
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
 - LinearGradientBrush.GetLinearColors
---

# LinearGradientBrush::GetLinearColors


## -description

The <b>LinearGradientBrush::GetLinearColors</b> method gets the starting color and ending color of this linear gradient brush.

## -parameters

### -param colors [out]

Type: <b>Color*</b>

Pointer to an array that receives the starting color and the ending color. The first color in the 
					<i>colors</i> array is the color at the starting boundary line of the gradient; the second color in the 
					<i>colors</i> array is the color at the ending boundary line.

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



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-setlinearcolors">LinearGradientBrush::SetLinearColors</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>



<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush">SolidBrush</a>