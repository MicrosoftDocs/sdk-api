---
UID: NF:gdipluseffects.Sharpen.GetParameters
title: Sharpen::GetParameters (gdipluseffects.h)
description: The Sharpen::GetParameters method gets the current values of the parameters of this Sharpen object.
helpviewer_keywords: ["GetParameters","GetParameters method [GDI+]","GetParameters method [GDI+]","Sharpen class","Sharpen class [GDI+]","GetParameters method","Sharpen.GetParameters","Sharpen::GetParameters","_gdiplus_CLASS_Sharpen_GetParameters_","gdiplus._gdiplus_CLASS_Sharpen_GetParameters_"]
old-location: gdiplus\_gdiplus_CLASS_Sharpen_GetParameters_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\sharpenclass\sharpenmethods\getparameters.htm
ms.date: 12/05/2018
ms.keywords: GetParameters, GetParameters method [GDI+], GetParameters method [GDI+],Sharpen class, Sharpen class [GDI+],GetParameters method, Sharpen.GetParameters, Sharpen::GetParameters, _gdiplus_CLASS_Sharpen_GetParameters_, gdiplus._gdiplus_CLASS_Sharpen_GetParameters_
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
 - Sharpen::GetParameters
 - gdipluseffects/Sharpen::GetParameters
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
 - Sharpen.GetParameters
---

# Sharpen::GetParameters


## -description

The <b>Sharpen::GetParameters</b> method gets the current values of the parameters of this <a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-sharpen">Sharpen</a> object.

## -parameters

### -param size [in]

Type: <b>UINT*</b>

Pointer to a <b>UINT</b> that specifies the size, in bytes, of a <a href="/windows/desktop/api/gdipluseffects/ns-gdipluseffects-sharpenparams">SharpenParams</a> structure.

### -param parameters [out]

Type: <b><a href="/windows/desktop/api/gdipluseffects/ns-gdipluseffects-sharpenparams">SharpenParams</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdipluseffects/ns-gdipluseffects-sharpenparams">SharpenParams</a> structure that receives the parameter values.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-sharpen">Sharpen</a>



<a href="/windows/desktop/api/gdipluseffects/nf-gdipluseffects-sharpen-setparameters">Sharpen::SetParameters</a>