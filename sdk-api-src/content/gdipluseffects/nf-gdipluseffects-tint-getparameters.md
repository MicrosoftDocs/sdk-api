---
UID: NF:gdipluseffects.Tint.GetParameters
title: Tint::GetParameters (gdipluseffects.h)
description: The Tint::GetParameters method gets the current values of the parameters of this Tint object.
helpviewer_keywords: ["GetParameters","GetParameters method [GDI+]","GetParameters method [GDI+]","Tint class","Tint class [GDI+]","GetParameters method","Tint.GetParameters","Tint::GetParameters","_gdiplus_CLASS_Tint_GetParameters_","gdiplus._gdiplus_CLASS_Tint_GetParameters_"]
old-location: gdiplus\_gdiplus_CLASS_Tint_GetParameters_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\tintclass\tintmethods\getparameters.htm
ms.date: 12/05/2018
ms.keywords: GetParameters, GetParameters method [GDI+], GetParameters method [GDI+],Tint class, Tint class [GDI+],GetParameters method, Tint.GetParameters, Tint::GetParameters, _gdiplus_CLASS_Tint_GetParameters_, gdiplus._gdiplus_CLASS_Tint_GetParameters_
f1_keywords:
- gdipluseffects/Tint.GetParameters
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
- Tint.GetParameters
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
ms.custom: 19H1
---

# Tint::GetParameters


## -description


The <b>Tint::GetParameters</b> method gets the current values of the parameters of this <a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/nl-gdipluseffects-tint">Tint</a> object.


## -parameters




### -param size [in]

Type: <b>UINT*</b>

Pointer to a <b>UINT</b> that specifies the size, in bytes, of a <a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/ns-gdipluseffects-tintparams">TintParams</a> structure.


### -param parameters [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/ns-gdipluseffects-tintparams">TintParams</a>*</b>

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/ns-gdipluseffects-tintparams">TintParams</a> structure that receives the parameter values.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/nl-gdipluseffects-tint">Tint</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/nf-gdipluseffects-tint-setparameters">Tint::SetParameters</a>
 

 

