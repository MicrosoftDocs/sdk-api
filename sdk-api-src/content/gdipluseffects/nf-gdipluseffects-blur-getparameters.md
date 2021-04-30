---
UID: NF:gdipluseffects.Blur.GetParameters
title: Blur::GetParameters (gdipluseffects.h)
description: The Blur::GetParameters method gets the current values of the parameters of this Blur object.
helpviewer_keywords: ["Blur class [GDI+]","GetParameters method","Blur.GetParameters","Blur::GetParameters","GetParameters","GetParameters method [GDI+]","GetParameters method [GDI+]","Blur class","_gdiplus_CLASS_Blur_GetParameters_","gdiplus._gdiplus_CLASS_Blur_GetParameters_"]
old-location: gdiplus\_gdiplus_CLASS_Blur_GetParameters_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\blurclass\blurmethods\getparameters.htm
ms.date: 12/05/2018
ms.keywords: Blur class [GDI+],GetParameters method, Blur.GetParameters, Blur::GetParameters, GetParameters, GetParameters method [GDI+], GetParameters method [GDI+],Blur class, _gdiplus_CLASS_Blur_GetParameters_, gdiplus._gdiplus_CLASS_Blur_GetParameters_
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
 - Blur::GetParameters
 - gdipluseffects/Blur::GetParameters
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
 - Blur.GetParameters
---

# Blur::GetParameters


## -description

The <b>Blur::GetParameters</b> method gets the current values of the parameters of this <a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-blur">Blur</a> object.

## -parameters

### -param size [in]

Type: <b>UINT*</b>

Pointer to a <b>UINT</b> that specifies the size, in bytes, of a <a href="/windows/desktop/api/gdipluseffects/ns-gdipluseffects-blurparams">BlurParams</a> structure.

### -param parameters [out]

Type: <b><a href="/windows/desktop/api/gdipluseffects/ns-gdipluseffects-blurparams">BlurParams</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdipluseffects/ns-gdipluseffects-blurparams">BlurParams</a> structure that receives the parameter values.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-blur">Blur</a>



<a href="/windows/desktop/api/gdipluseffects/nf-gdipluseffects-blur-setparameters">Blur::SetParameters</a>



<a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-sharpen">Sharpen</a>