---
UID: NF:gdipluseffects.HueSaturationLightness.GetParameters
title: HueSaturationLightness::GetParameters (gdipluseffects.h)
author: windows-sdk-content
description: The HueSaturationLightness::GetParameters method gets the current values of the parameters of this HueSaturationLightness object.
old-location: gdiplus\_gdiplus_CLASS_HueSaturationLightness_GetParameters_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\huesaturationlightnessclass\huesaturationlightnessmethods\getparameters.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetParameters, GetParameters method [GDI+], GetParameters method [GDI+],HueSaturationLightness class, HueSaturationLightness class [GDI+],GetParameters method, HueSaturationLightness.GetParameters, HueSaturationLightness::GetParameters, _gdiplus_CLASS_HueSaturationLightness_GetParameters_, gdiplus._gdiplus_CLASS_HueSaturationLightness_GetParameters_
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
---

# HueSaturationLightness::GetParameters


## -description


The <b>HueSaturationLightness::GetParameters</b> method gets the current values of the parameters of this <a href="https://msdn.microsoft.com/en-us/library/ms534461(v=VS.85).aspx">HueSaturationLightness</a> object.


## -parameters




### -param size [in]

Type: <b>UINT*</b>

Pointer to a <b>UINT</b> that specifies the size of a <a href="https://msdn.microsoft.com/en-us/library/ms534069(v=VS.85).aspx">HueSaturationLightnessParams</a> structure.


### -param parameters [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534069(v=VS.85).aspx">HueSaturationLightnessParams</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534069(v=VS.85).aspx">HueSaturationLightnessParams</a> structure that receives the parameter values.


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534461(v=VS.85).aspx">HueSaturationLightness</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535442(v=VS.85).aspx">HueSaturationLightness::SetParameters</a>
 

 

