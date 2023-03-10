---
UID: NF:gdiplusbrush.LinearGradientBrush.SetGammaCorrection
title: LinearGradientBrush::SetGammaCorrection (gdiplusbrush.h)
description: The LinearGradientBrush::SetGammaCorrection method specifies whether gamma correction is enabled for this linear gradient brush.
helpviewer_keywords: ["LinearGradientBrush class [GDI+]","SetGammaCorrection method","LinearGradientBrush.SetGammaCorrection","LinearGradientBrush::SetGammaCorrection","SetGammaCorrection","SetGammaCorrection method [GDI+]","SetGammaCorrection method [GDI+]","LinearGradientBrush class","_gdiplus_CLASS_LinearGradientBrush_SetGammaCorrection_useGammaCorrection_","gdiplus._gdiplus_CLASS_LinearGradientBrush_SetGammaCorrection_useGammaCorrection_"]
old-location: gdiplus\_gdiplus_CLASS_LinearGradientBrush_SetGammaCorrection_useGammaCorrection_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\lineargradientbrushclass\lineargradientbrushmethods\setgammacorrection.htm
ms.date: 12/05/2018
ms.keywords: LinearGradientBrush class [GDI+],SetGammaCorrection method, LinearGradientBrush.SetGammaCorrection, LinearGradientBrush::SetGammaCorrection, SetGammaCorrection, SetGammaCorrection method [GDI+], SetGammaCorrection method [GDI+],LinearGradientBrush class, _gdiplus_CLASS_LinearGradientBrush_SetGammaCorrection_useGammaCorrection_, gdiplus._gdiplus_CLASS_LinearGradientBrush_SetGammaCorrection_useGammaCorrection_
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
 - LinearGradientBrush::SetGammaCorrection
 - gdiplusbrush/LinearGradientBrush::SetGammaCorrection
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
 - LinearGradientBrush.SetGammaCorrection
---

# LinearGradientBrush::SetGammaCorrection


## -description

The <b>LinearGradientBrush::SetGammaCorrection</b> method specifies whether gamma correction is enabled for this linear gradient brush.

## -parameters

### -param useGammaCorrection [in]

Type: <b>BOOL</b>

Boolean value that specifies whether gamma correction occurs during rendering. <b>TRUE</b> specifies that gamma correction is enabled, and <b>FALSE</b> specifies that gamma correction is not enabled. By default, gamma correction is disabled during construction of a 
					<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush">LinearGradientBrush</a> object.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

Gamma correction is often done to match the intensity contrast of the gradient to the ability of the human eye to perceive intensity changes.

## -see-also

<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush">LinearGradientBrush</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-getgammacorrection">LinearGradientBrush::GetGammaCorrection</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>