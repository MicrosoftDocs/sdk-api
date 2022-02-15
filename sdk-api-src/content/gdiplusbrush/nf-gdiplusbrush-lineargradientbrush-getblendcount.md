---
UID: NF:gdiplusbrush.LinearGradientBrush.GetBlendCount
title: LinearGradientBrush::GetBlendCount (gdiplusbrush.h)
description: The LinearGradientBrush::GetBlendCount method gets the number of blend factors currently set for this LinearGradientBrush object.
helpviewer_keywords: ["GetBlendCount","GetBlendCount method [GDI+]","GetBlendCount method [GDI+]","LinearGradientBrush class","LinearGradientBrush class [GDI+]","GetBlendCount method","LinearGradientBrush.GetBlendCount","LinearGradientBrush::GetBlendCount","_gdiplus_CLASS_LinearGradientBrush_GetBlendCount_","gdiplus._gdiplus_CLASS_LinearGradientBrush_GetBlendCount_"]
old-location: gdiplus\_gdiplus_CLASS_LinearGradientBrush_GetBlendCount_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\lineargradientbrushclass\lineargradientbrushmethods\getblendcount.htm
ms.date: 12/05/2018
ms.keywords: GetBlendCount, GetBlendCount method [GDI+], GetBlendCount method [GDI+],LinearGradientBrush class, LinearGradientBrush class [GDI+],GetBlendCount method, LinearGradientBrush.GetBlendCount, LinearGradientBrush::GetBlendCount, _gdiplus_CLASS_LinearGradientBrush_GetBlendCount_, gdiplus._gdiplus_CLASS_LinearGradientBrush_GetBlendCount_
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
 - LinearGradientBrush::GetBlendCount
 - gdiplusbrush/LinearGradientBrush::GetBlendCount
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
 - LinearGradientBrush.GetBlendCount
---

# LinearGradientBrush::GetBlendCount


## -description

The <b>LinearGradientBrush::GetBlendCount</b> method gets the number of blend factors currently set for this 
			<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush">LinearGradientBrush</a> object.



## -returns

Type: <b>INT</b>

This method returns the number of blend factors currently set for this 
						<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush">LinearGradientBrush</a> object. If no custom blend has been set by using <a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-setblend">LinearGradientBrush::SetBlend</a>, or if invalid positions were passed to <b>LinearGradientBrush::SetBlend</b>, then <a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-getblend">LinearGradientBrush::GetBlend</a> returns 1.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>



<a href="/windows/desktop/gdiplus/-gdiplus-filling-shapes-with-a-gradient-brush-use">Filling Shapes with a Gradient Brush</a>



<a href="/windows/desktop/gdiplus/-gdiplus-filling-a-shape-with-a-color-gradient-use">Filling a Shape with a Color Gradient</a>



<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush">LinearGradientBrush</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-getblend">LinearGradientBrush::GetBlend</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-setblend">LinearGradientBrush::SetBlend</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>
