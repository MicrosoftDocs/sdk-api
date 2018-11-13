---
UID: NF:gdipluseffects.HueSaturationLightness.GetParameters
title: HueSaturationLightness::GetParameters
author: windows-sdk-content
description: The HueSaturationLightness::GetParameters method gets the current values of the parameters of this HueSaturationLightness object.
old-location: gdiplus\_gdiplus_CLASS_HueSaturationLightness_GetParameters_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\huesaturationlightnessclass\huesaturationlightnessmethods\getparameters.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetParameters, GetParameters method [GDI+], GetParameters method [GDI+],HueSaturationLightness class, HueSaturationLightness class [GDI+],GetParameters method, HueSaturationLightness.GetParameters, HueSaturationLightness::GetParameters, _gdiplus_CLASS_HueSaturationLightness_GetParameters_, gdiplus._gdiplus_CLASS_HueSaturationLightness_GetParameters_
ms.prod: windows-hardware
ms.technology: windows-devices
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


The <b>HueSaturationLightness::GetParameters</b> method gets the current values of the parameters of this <a href="https://msdn.microsoft.com/3bb652eb-62f0-4948-9484-4439dc9bd54e">HueSaturationLightness</a> object.


## -parameters




### -param size [in]

Type: <b>UINT*</b>

Pointer to a <b>UINT</b> that specifies the size of a <a href="https://msdn.microsoft.com/d46ef884-ac73-4fa0-8c4d-d033ac1ed406">HueSaturationLightnessParams</a> structure.


### -param parameters [out]

Type: <b><a href="https://msdn.microsoft.com/d46ef884-ac73-4fa0-8c4d-d033ac1ed406">HueSaturationLightnessParams</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/d46ef884-ac73-4fa0-8c4d-d033ac1ed406">HueSaturationLightnessParams</a> structure that receives the parameter values.


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/3bb652eb-62f0-4948-9484-4439dc9bd54e">HueSaturationLightness</a>



<a href="https://msdn.microsoft.com/40039dc9-48c5-40b3-9fcc-03f30b32e208">HueSaturationLightness::SetParameters</a>
 

 

