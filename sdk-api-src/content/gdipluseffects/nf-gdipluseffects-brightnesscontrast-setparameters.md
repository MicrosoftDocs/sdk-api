---
UID: NF:gdipluseffects.BrightnessContrast.SetParameters
title: BrightnessContrast::SetParameters (gdipluseffects.h)
description: The BrightnessContrast::SetParameters method sets the parameters of this BrightnessContrast object.
helpviewer_keywords: ["BrightnessContrast class [GDI+]","SetParameters method","BrightnessContrast.SetParameters","BrightnessContrast::SetParameters","SetParameters","SetParameters method [GDI+]","SetParameters method [GDI+]","BrightnessContrast class","_gdiplus_CLASS_BrightnessContrast_SetParameters_","gdiplus._gdiplus_CLASS_BrightnessContrast_SetParameters_"]
old-location: gdiplus\_gdiplus_CLASS_BrightnessContrast_SetParameters_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\brightnesscontrastclass\brightnesscontrastmethods\setparameters.htm
ms.date: 12/05/2018
ms.keywords: BrightnessContrast class [GDI+],SetParameters method, BrightnessContrast.SetParameters, BrightnessContrast::SetParameters, SetParameters, SetParameters method [GDI+], SetParameters method [GDI+],BrightnessContrast class, _gdiplus_CLASS_BrightnessContrast_SetParameters_, gdiplus._gdiplus_CLASS_BrightnessContrast_SetParameters_
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
 - BrightnessContrast::SetParameters
 - gdipluseffects/BrightnessContrast::SetParameters
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
 - BrightnessContrast.SetParameters
---

# BrightnessContrast::SetParameters


## -description

The <b>BrightnessContrast::SetParameters</b> method sets the parameters of this <a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-brightnesscontrast">BrightnessContrast</a> object.

## -parameters

### -param parameters [in]

Type: <b>const <a href="/windows/desktop/api/gdipluseffects/ns-gdipluseffects-brightnesscontrastparams">BrightnessContrastParams</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdipluseffects/ns-gdipluseffects-brightnesscontrastparams">BrightnessContrastParams</a> structure that specifies the parameters.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-brightnesscontrast">BrightnessContrast</a>



<a href="/windows/desktop/api/gdipluseffects/nf-gdipluseffects-brightnesscontrast-getparameters">BrightnessContrast::GetParameters</a>