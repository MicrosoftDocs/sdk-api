---
UID: NF:gdipluseffects.ColorMatrixEffect.SetParameters
title: ColorMatrixEffect::SetParameters (gdipluseffects.h)
description: The ColorMatrixEffect::SetParameters method sets the 5x5 color matrix of this ColorMatrixEffect object.
old-location: gdiplus\_gdiplus_CLASS_ColorMatrixEffect_SetParameters_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\colormatrixeffectclass\colormatrixeffectmethods\setparameters.htm
ms.date: 12/05/2018
ms.keywords: ColorMatrixEffect class [GDI+],SetParameters method, ColorMatrixEffect.SetParameters, ColorMatrixEffect::SetParameters, SetParameters, SetParameters method [GDI+], SetParameters method [GDI+],ColorMatrixEffect class, _gdiplus_CLASS_ColorMatrixEffect_SetParameters_, gdiplus._gdiplus_CLASS_ColorMatrixEffect_SetParameters_
f1_keywords:
- gdipluseffects/ColorMatrixEffect.SetParameters
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Gdiplus.dll
api_name:
- ColorMatrixEffect.SetParameters
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
ms.custom: 19H1
---

# ColorMatrixEffect::SetParameters


## -description


The <b>ColorMatrixEffect::SetParameters</b> method sets the 5x5 color matrix of this <a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/nl-gdipluseffects-colormatrixeffect">ColorMatrixEffect</a> object.


## -parameters




### -param matrix [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix">ColorMatrix</a>*</b>

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix">ColorMatrix</a> object that specifies the 5x5 color matrix. 


## -returns



Type: <strong>Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/nl-gdipluseffects-colormatrixeffect">ColorMatrixEffect</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/nf-gdipluseffects-colormatrixeffect-getparameters">ColorMatrixEffect::GetParameters</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-recoloring-use">Recoloring</a>
 

 

