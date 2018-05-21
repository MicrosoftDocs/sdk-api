---
UID: NL:gdipluseffects.HueSaturationLightness
title: HueSaturationLightness
author: windows-driver-content
description: The HueSaturationLightness class enables you to change the hue, saturation, and lightness of a bitmap.
old-location: gdiplus\_gdiplus_CLASS_HueSaturationLightness_Class.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\huesaturationlightness.htm
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: HueSaturationLightness, HueSaturationLightness class [GDI+], HueSaturationLightness class [GDI+],described, _gdiplus_CLASS_HueSaturationLightness_Class, gdiplus._gdiplus_CLASS_HueSaturationLightness_Class, gdipluseffects/HueSaturationLightness
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: class
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	gdipluseffects.h
api_name:
-	HueSaturationLightness
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.1
---

# HueSaturationLightness class


## -description


The <b>HueSaturationLightness</b> class enables you to change the hue, saturation, and lightness of a bitmap. Pass the address of a <b>HueSaturationLightness</b> object to the <a href="https://msdn.microsoft.com/cb85a7ac-5af0-45c7-8035-d7bc2827af6a">Graphics::DrawImage</a> method or to the <a href="https://msdn.microsoft.com/6b3d0a2f-acff-47a7-bc9f-6e9d659f683c">Bitmap::ApplyEffect</a> method. To specify the magnitudes of the changes in hue, saturation, and lightness, pass a <a href="https://msdn.microsoft.com/d46ef884-ac73-4fa0-8c4d-d033ac1ed406">HueSaturationLightnessParams</a> structure to the <a href="https://msdn.microsoft.com/40039dc9-48c5-40b3-9fcc-03f30b32e208">HueSaturationLightness::SetParameters</a> method of a <b>HueSaturationLightness</b> object.

