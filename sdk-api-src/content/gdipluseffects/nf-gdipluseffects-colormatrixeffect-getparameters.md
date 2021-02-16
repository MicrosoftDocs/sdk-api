---
UID: NF:gdipluseffects.ColorMatrixEffect.GetParameters
title: ColorMatrixEffect::GetParameters (gdipluseffects.h)
description: The ColorMatrixEffect::GetParameters method gets the elements of the current 5x5 color matrix of this ColorMatrixEffect object.
helpviewer_keywords: ["ColorMatrixEffect class [GDI+]","GetParameters method","ColorMatrixEffect.GetParameters","ColorMatrixEffect::GetParameters","GetParameters","GetParameters method [GDI+]","GetParameters method [GDI+]","ColorMatrixEffect class","_gdiplus_CLASS_ColorMatrixEffect_GetParameters_","gdiplus._gdiplus_CLASS_ColorMatrixEffect_GetParameters_"]
old-location: gdiplus\_gdiplus_CLASS_ColorMatrixEffect_GetParameters_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\colormatrixeffectclass\colormatrixeffectmethods\getparameters.htm
ms.date: 12/05/2018
ms.keywords: ColorMatrixEffect class [GDI+],GetParameters method, ColorMatrixEffect.GetParameters, ColorMatrixEffect::GetParameters, GetParameters, GetParameters method [GDI+], GetParameters method [GDI+],ColorMatrixEffect class, _gdiplus_CLASS_ColorMatrixEffect_GetParameters_, gdiplus._gdiplus_CLASS_ColorMatrixEffect_GetParameters_
req.header: gdipluseffects.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.product: GDI+ 1.1
ms.custom: 19H1
f1_keywords:
 - ColorMatrixEffect::GetParameters
 - gdipluseffects/ColorMatrixEffect::GetParameters
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
 - ColorMatrixEffect.GetParameters
---

# ColorMatrixEffect::GetParameters


## -description

The <b>ColorMatrixEffect::GetParameters</b> method gets the elements of the current 5x5 color matrix of this <a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-colormatrixeffect">ColorMatrixEffect</a> object.

## -parameters

### -param size [in]

Type: <b>UINT*</b>

Pointer to a <b>UINT</b> that specifies the size, in bytes, of a <a href="/windows/desktop/api/gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix">ColorMatrix</a> structure.

### -param matrix [out]

Type: <b><a href="/windows/desktop/api/gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix">ColorMatrix</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix">ColorMatrix</a> structure that receives the elements of the color matrix.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-colormatrixeffect">ColorMatrixEffect</a>



<a href="/windows/desktop/api/gdipluseffects/nf-gdipluseffects-colormatrixeffect-setparameters">ColorMatrixEffect::SetParameters</a>