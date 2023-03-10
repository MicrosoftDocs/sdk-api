---
UID: NF:gdiplusbrush.LinearGradientBrush.SetLinearColors
title: LinearGradientBrush::SetLinearColors (gdiplusbrush.h)
description: The LinearGradientBrush::SetLinearColors method sets the starting color and ending color of this linear gradient brush.
helpviewer_keywords: ["LinearGradientBrush class [GDI+]","SetLinearColors method","LinearGradientBrush.SetLinearColors","LinearGradientBrush::SetLinearColors","SetLinearColors","SetLinearColors method [GDI+]","SetLinearColors method [GDI+]","LinearGradientBrush class","_gdiplus_CLASS_LinearGradientBrush_SetLinearColors_color1_color2_","gdiplus._gdiplus_CLASS_LinearGradientBrush_SetLinearColors_color1_color2_"]
old-location: gdiplus\_gdiplus_CLASS_LinearGradientBrush_SetLinearColors_color1_color2_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\lineargradientbrushclass\lineargradientbrushmethods\setlinearcolors.htm
ms.date: 12/05/2018
ms.keywords: LinearGradientBrush class [GDI+],SetLinearColors method, LinearGradientBrush.SetLinearColors, LinearGradientBrush::SetLinearColors, SetLinearColors, SetLinearColors method [GDI+], SetLinearColors method [GDI+],LinearGradientBrush class, _gdiplus_CLASS_LinearGradientBrush_SetLinearColors_color1_color2_, gdiplus._gdiplus_CLASS_LinearGradientBrush_SetLinearColors_color1_color2_
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
 - LinearGradientBrush::SetLinearColors
 - gdiplusbrush/LinearGradientBrush::SetLinearColors
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
 - LinearGradientBrush.SetLinearColors
---

# LinearGradientBrush::SetLinearColors


## -description

The <b>LinearGradientBrush::SetLinearColors</b> method sets the starting color and ending color of this linear gradient brush.

## -parameters

### -param color1 [in]

Type: <b>const Color&amp;</b>

Reference to a <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a> object that specifies the color at the starting boundary line of this linear gradient brush.

### -param color2 [in]

Type: <b>const Color&amp;</b>

Reference to a <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a> object that specifies the color at the ending boundary line of this linear gradient brush.

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



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-getlinearcolors">LinearGradientBrush::GetLinearColors</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-setinterpolationcolors">LinearGradientBrush::SetInterpolationColors</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>