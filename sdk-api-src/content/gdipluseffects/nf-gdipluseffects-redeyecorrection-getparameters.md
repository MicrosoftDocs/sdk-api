---
UID: NF:gdipluseffects.RedEyeCorrection.GetParameters
title: RedEyeCorrection::GetParameters (gdipluseffects.h)
description: The RedEyeCorrection::GetParameters method gets the current values of the parameters of this RedEyeCorrection object.
helpviewer_keywords: ["GetParameters","GetParameters method [GDI+]","GetParameters method [GDI+]","RedEyeCorrection class","RedEyeCorrection class [GDI+]","GetParameters method","RedEyeCorrection.GetParameters","RedEyeCorrection::GetParameters","_gdiplus_CLASS_RedEyeCorrection_GetParameters_","gdiplus._gdiplus_CLASS_RedEyeCorrection_GetParameters_"]
old-location: gdiplus\_gdiplus_CLASS_RedEyeCorrection_GetParameters_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\redeyecorrectionclass\redeyecorrectionmethods\getparameters.htm
ms.date: 12/05/2018
ms.keywords: GetParameters, GetParameters method [GDI+], GetParameters method [GDI+],RedEyeCorrection class, RedEyeCorrection class [GDI+],GetParameters method, RedEyeCorrection.GetParameters, RedEyeCorrection::GetParameters, _gdiplus_CLASS_RedEyeCorrection_GetParameters_, gdiplus._gdiplus_CLASS_RedEyeCorrection_GetParameters_
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
 - RedEyeCorrection::GetParameters
 - gdipluseffects/RedEyeCorrection::GetParameters
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
 - RedEyeCorrection.GetParameters
---

# RedEyeCorrection::GetParameters


## -description

The <b>RedEyeCorrection::GetParameters</b> method gets the current values of the parameters of this <a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-redeyecorrection">RedEyeCorrection</a> object.

## -parameters

### -param size [in]

Type: <b>UINT*</b>

The size, in bytes, of the buffer pointed to by the <i>parameters</i> parameter.

### -param parameters [out]

Type: <b><a href="/windows/desktop/api/gdipluseffects/ns-gdipluseffects-redeyecorrectionparams">RedEyeCorrectionParams</a>*</b>

Pointer to a buffer that is large enough to receive a <a href="/windows/desktop/api/gdipluseffects/ns-gdipluseffects-redeyecorrectionparams">RedEyeCorrectionParams</a> structure followed by an array of RECT structures. To determine the total size of the required buffer, call the GetParameterSize method of the <a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-redeyecorrection">RedEyeCorrection</a> object whose parameters you want to retrieve.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-redeyecorrection">RedEyeCorrection</a>



<a href="/windows/desktop/api/gdipluseffects/nf-gdipluseffects-redeyecorrection-setparameters">RedEyeCorrection::SetParameters</a>