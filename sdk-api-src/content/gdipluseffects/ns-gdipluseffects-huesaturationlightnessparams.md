---
UID: NS:gdipluseffects.HueSaturationLightnessParams
title: HueSaturationLightnessParams
author: windows-sdk-content
description: The HueSaturationLightnessParams structure contains members that specify hue, saturation and lightness adjustments to a bitmap.
old-location: gdiplus\_gdiplus_STRUC_HueSaturationLightnessParams.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\structures\huesaturationlightnessparams.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: HueSaturationLightnessParams, HueSaturationLightnessParams structure [GDI+], _gdiplus_STRUC_HueSaturationLightnessParams, gdiplus._gdiplus_STRUC_HueSaturationLightnessParams, gdipluseffects/HueSaturationLightnessParams
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdipluseffects.h
api_name:
 - HueSaturationLightnessParams
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
---

# HueSaturationLightnessParams structure


## -description


The <b>HueSaturationLightnessParams</b> structure contains members that specify hue, saturation and lightness adjustments to a bitmap.

You can adjust the hue, saturation, and lightness of a bitmap by following these steps.
<ol>
<li>Create and initialize a <b>HueSaturationLightnessParams</b> structure.</li>
<li>Pass the address of the <b>HueSaturationLightnessParams</b> structure to the <a href="https://msdn.microsoft.com/en-us/library/ms535442(v=VS.85).aspx">HueSaturationLightness::SetParameters</a> method of a <a href="https://msdn.microsoft.com/en-us/library/ms534461(v=VS.85).aspx">HueSaturationLightness</a> object.</li>
<li>Pass the address of the <a href="https://msdn.microsoft.com/en-us/library/ms534461(v=VS.85).aspx">HueSaturationLightness</a> object to the <a href="https://msdn.microsoft.com/en-us/library/ms536058(v=VS.85).aspx">Graphics::DrawImage</a> method or to the <a href="https://msdn.microsoft.com/en-us/library/ms536284(v=VS.85).aspx">Bitmap::ApplyEffect</a> method.</li>
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

