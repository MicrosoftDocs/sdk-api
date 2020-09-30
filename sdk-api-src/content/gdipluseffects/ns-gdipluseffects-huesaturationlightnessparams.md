---
UID: NS:gdipluseffects.HueSaturationLightnessParams
title: HueSaturationLightnessParams (gdipluseffects.h)
description: The HueSaturationLightnessParams structure contains members that specify hue, saturation and lightness adjustments to a bitmap.
helpviewer_keywords: ["HueSaturationLightnessParams","HueSaturationLightnessParams structure [GDI+]","_gdiplus_STRUC_HueSaturationLightnessParams","gdiplus._gdiplus_STRUC_HueSaturationLightnessParams","gdipluseffects/HueSaturationLightnessParams"]
old-location: gdiplus\_gdiplus_STRUC_HueSaturationLightnessParams.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\structures\huesaturationlightnessparams.htm
ms.date: 12/05/2018
ms.keywords: HueSaturationLightnessParams, HueSaturationLightnessParams structure [GDI+], _gdiplus_STRUC_HueSaturationLightnessParams, gdiplus._gdiplus_STRUC_HueSaturationLightnessParams, gdipluseffects/HueSaturationLightnessParams
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
ms.custom: 19H1
f1_keywords:
 - HueSaturationLightnessParams
 - gdipluseffects/HueSaturationLightnessParams
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdipluseffects.h
api_name:
 - HueSaturationLightnessParams
---

# HueSaturationLightnessParams structure


## -description

The <b>HueSaturationLightnessParams</b> structure contains members that specify hue, saturation and lightness adjustments to a bitmap.

You can adjust the hue, saturation, and lightness of a bitmap by following these steps.
<ol>
<li>Create and initialize a <b>HueSaturationLightnessParams</b> structure.</li>
<li>Pass the address of the <b>HueSaturationLightnessParams</b> structure to the <a href="/windows/desktop/api/gdipluseffects/nf-gdipluseffects-huesaturationlightness-setparameters">HueSaturationLightness::SetParameters</a> method of a <a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-huesaturationlightness">HueSaturationLightness</a> object.</li>
<li>Pass the address of the <a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-huesaturationlightness">HueSaturationLightness</a> object to the <a href="/previous-versions/ms536058(v=vs.85)">Graphics::DrawImage</a> method or to the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-applyeffect(inbitmap_inint_ineffect_inrect_outrect_outbitmap)">Bitmap::ApplyEffect</a> method.</li>
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