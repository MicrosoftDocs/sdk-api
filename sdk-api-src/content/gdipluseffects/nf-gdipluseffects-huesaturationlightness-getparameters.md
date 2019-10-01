---
UID: NF:gdipluseffects.HueSaturationLightness.GetParameters
title: HueSaturationLightness::GetParameters (gdipluseffects.h)
author: windows-sdk-content
description: The HueSaturationLightness::GetParameters method gets the current values of the parameters of this HueSaturationLightness object.
old-location: gdiplus\_gdiplus_CLASS_HueSaturationLightness_GetParameters_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\huesaturationlightnessclass\huesaturationlightnessmethods\getparameters.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetParameters, GetParameters method [GDI+], GetParameters method [GDI+],HueSaturationLightness class, HueSaturationLightness class [GDI+],GetParameters method, HueSaturationLightness.GetParameters, HueSaturationLightness::GetParameters, _gdiplus_CLASS_HueSaturationLightness_GetParameters_, gdiplus._gdiplus_CLASS_HueSaturationLightness_GetParameters_
ms.topic: method
f1_keywords: 
 - "gdipluseffects/HueSaturationLightness.GetParameters"
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
 - HueSaturationLightness.GetParameters
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
ms.custom: 19H1
---

# HueSaturationLightness::GetParameters


## -description


The <b>HueSaturationLightness::GetParameters</b> method gets the current values of the parameters of this <a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/nl-gdipluseffects-huesaturationlightness">HueSaturationLightness</a> object.


## -parameters




### -param size [in]

Type: <b>UINT*</b>

Pointer to a <b>UINT</b> that specifies the size of a <a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/ns-gdipluseffects-huesaturationlightnessparams">HueSaturationLightnessParams</a> structure.


### -param parameters [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/ns-gdipluseffects-huesaturationlightnessparams">HueSaturationLightnessParams</a>*</b>

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/ns-gdipluseffects-huesaturationlightnessparams">HueSaturationLightnessParams</a> structure that receives the parameter values.


## -returns



Type: <strong>Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/nl-gdipluseffects-huesaturationlightness">HueSaturationLightness</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/nf-gdipluseffects-huesaturationlightness-setparameters">HueSaturationLightness::SetParameters</a>
 

 

