---
UID: NS:gdipluseffects.HueSaturationLightnessParams
title: HueSaturationLightnessParams
author: windows-sdk-content
description: The HueSaturationLightnessParams structure contains members that specify hue, saturation and lightness adjustments to a bitmap.
old-location: gdiplus\_gdiplus_STRUC_HueSaturationLightnessParams.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\structures\huesaturationlightnessparams.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: HueSaturationLightnessParams, HueSaturationLightnessParams structure [GDI+], _gdiplus_STRUC_HueSaturationLightnessParams, gdiplus._gdiplus_STRUC_HueSaturationLightnessParams, gdipluseffects/HueSaturationLightnessParams
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Gdipluseffects.h
api_name:
-	HueSaturationLightnessParams
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# HueSaturationLightnessParams structure


## -description


The <b>HueSaturationLightnessParams</b> structure contains members that specify hue, saturation and lightness adjustments to a bitmap.

You can adjust the hue, saturation, and lightness of a bitmap by following these steps.
<ol>
<li>Create and initialize a <b>HueSaturationLightnessParams</b> structure.</li>
<li>Pass the address of the <b>HueSaturationLightnessParams</b> structure to the <a href="https://msdn.microsoft.com/40039dc9-48c5-40b3-9fcc-03f30b32e208">HueSaturationLightness::SetParameters</a> method of a <a href="https://msdn.microsoft.com/3bb652eb-62f0-4948-9484-4439dc9bd54e">HueSaturationLightness</a> object.</li>
<li>Pass the address of the <a href="https://msdn.microsoft.com/3bb652eb-62f0-4948-9484-4439dc9bd54e">HueSaturationLightness</a> object to the <a href="https://msdn.microsoft.com/cb85a7ac-5af0-45c7-8035-d7bc2827af6a">Graphics::DrawImage</a> method or to the <a href="https://msdn.microsoft.com/6b3d0a2f-acff-47a7-bc9f-6e9d659f683c">Bitmap::ApplyEffect</a> method.</li>
</ol>

## -struct-fields




### -field hueLevel

Type: <b>INT</b>

Integer in the range -180 through 180 that specifies the change in hue. A value of 0 specifies no change. Positive values specify counterclockwise rotation on the color wheel. Negative values specify clockwise rotation on the color wheel.


### -field saturationLevel

Type: <b>INT</b>

Integer in the range -100 through 100 that specifies the change in saturation. A value of 0 specifies no change. Positive values specify increased saturation and negative values specify decreased saturation.


### -field lightnessLevel

Type: <b>INT</b>

Integer in the range -100 through 100 that specifies the change in lightness. A value of 0 specifies no change. Positive values specify increased lightness and negative values specify decreased lightness.

