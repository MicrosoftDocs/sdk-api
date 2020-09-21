---
UID: NF:gdipluseffects.BrightnessContrast.GetParameters
title: BrightnessContrast::GetParameters (gdipluseffects.h)
description: The BrightnessContrast::GetParameters method gets the current values of the parameters of this BrightnessContrast object.
helpviewer_keywords: ["BrightnessContrast class [GDI+]","GetParameters method","BrightnessContrast.GetParameters","BrightnessContrast::GetParameters","GetParameters","GetParameters method [GDI+]","GetParameters method [GDI+]","BrightnessContrast class","_gdiplus_CLASS_BrightnessContrast_GetParameters_","gdiplus._gdiplus_CLASS_BrightnessContrast_GetParameters_"]
old-location: gdiplus\_gdiplus_CLASS_BrightnessContrast_GetParameters_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\brightnesscontrastclass\brightnesscontrastmethods\getparameters.htm
ms.date: 12/05/2018
ms.keywords: BrightnessContrast class [GDI+],GetParameters method, BrightnessContrast.GetParameters, BrightnessContrast::GetParameters, GetParameters, GetParameters method [GDI+], GetParameters method [GDI+],BrightnessContrast class, _gdiplus_CLASS_BrightnessContrast_GetParameters_, gdiplus._gdiplus_CLASS_BrightnessContrast_GetParameters_
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
 - BrightnessContrast::GetParameters
 - gdipluseffects/BrightnessContrast::GetParameters
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
 - BrightnessContrast.GetParameters
---

# BrightnessContrast::GetParameters


## -description

The <b>BrightnessContrast::GetParameters</b> method gets the current values of the parameters of this <a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-brightnesscontrast">BrightnessContrast</a> object.

## -parameters

### -param size [in]

Type: <b>UINT*</b>

Pointer to a <b>UINT</b> that specifies the size, in bytes, of a <a href="/windows/desktop/api/gdipluseffects/ns-gdipluseffects-brightnesscontrastparams">BrightnessContrastParams</a> structure.

### -param parameters [out]

Type: <b><a href="/windows/desktop/api/gdipluseffects/ns-gdipluseffects-brightnesscontrastparams">BrightnessContrastParams</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdipluseffects/ns-gdipluseffects-brightnesscontrastparams">BrightnessContrastParams</a> structure that receives the parameter values.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-brightnesscontrast">BrightnessContrast</a>



<a href="/windows/desktop/api/gdipluseffects/nf-gdipluseffects-brightnesscontrast-setparameters">BrightnessContrast::SetParameters</a>