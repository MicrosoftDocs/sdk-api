---
UID: NL:gdipluseffects.HueSaturationLightness
title: HueSaturationLightness (gdipluseffects.h)
description: The HueSaturationLightness class enables you to change the hue, saturation, and lightness of a bitmap.
helpviewer_keywords: ["HueSaturationLightness","HueSaturationLightness class [GDI+]","HueSaturationLightness class [GDI+]","described","_gdiplus_CLASS_HueSaturationLightness_Class","gdiplus._gdiplus_CLASS_HueSaturationLightness_Class","gdipluseffects/HueSaturationLightness"]
old-location: gdiplus\_gdiplus_CLASS_HueSaturationLightness_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\huesaturationlightness.htm
ms.date: 12/05/2018
ms.keywords: HueSaturationLightness, HueSaturationLightness class [GDI+], HueSaturationLightness class [GDI+],described, _gdiplus_CLASS_HueSaturationLightness_Class, gdiplus._gdiplus_CLASS_HueSaturationLightness_Class, gdipluseffects/HueSaturationLightness
req.header: gdipluseffects.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
ms.custom: 19H1
f1_keywords:
 - HueSaturationLightness
 - gdipluseffects/HueSaturationLightness
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - gdipluseffects.h
api_name:
 - HueSaturationLightness
---

# HueSaturationLightness class


## -description

The <b>HueSaturationLightness</b> class enables you to change the hue, saturation, and lightness of a bitmap. Pass the address of a <b>HueSaturationLightness</b> object to the <a href="/previous-versions/ms536058(v=vs.85)">Graphics::DrawImage</a> method or to the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-applyeffect(inbitmap_inint_ineffect_inrect_outrect_outbitmap)">Bitmap::ApplyEffect</a> method. To specify the magnitudes of the changes in hue, saturation, and lightness, pass a <a href="/windows/desktop/api/gdipluseffects/ns-gdipluseffects-huesaturationlightnessparams">HueSaturationLightnessParams</a> structure to the <a href="/windows/desktop/api/gdipluseffects/nf-gdipluseffects-huesaturationlightness-setparameters">HueSaturationLightness::SetParameters</a> method of a <b>HueSaturationLightness</b> object.