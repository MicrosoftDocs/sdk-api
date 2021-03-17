---
UID: NL:gdipluseffects.ColorCurve
title: ColorCurve (gdipluseffects.h)
description: The ColorCurve class encompasses eight separate adjustments:\_exposure, density, contrast, highlight, shadow, midtone, white saturation, and black saturation.
helpviewer_keywords: ["ColorCurve","ColorCurve class [GDI+]","ColorCurve class [GDI+]","described","_gdiplus_CLASS_ColorCurve_Class","gdiplus._gdiplus_CLASS_ColorCurve_Class","gdipluseffects/ColorCurve"]
old-location: gdiplus\_gdiplus_CLASS_ColorCurve_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\colorcurve.htm
ms.date: 12/05/2018
ms.keywords: ColorCurve, ColorCurve class [GDI+], ColorCurve class [GDI+],described, _gdiplus_CLASS_ColorCurve_Class, gdiplus._gdiplus_CLASS_ColorCurve_Class, gdipluseffects/ColorCurve
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
 - ColorCurve
 - gdipluseffects/ColorCurve
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
 - ColorCurve
---

# ColorCurve class


## -description

The <b>ColorCurve</b> class encompasses eight separate adjustments: exposure, density, contrast, highlight, shadow, midtone, white saturation, and black saturation. You can apply one of those adjustments to a bitmap by passing the address of a <b>ColorCurve</b> object to the <a href="/previous-versions/ms536058(v=vs.85)">Graphics::DrawImage</a> method or to the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-applyeffect(inbitmap_inint_ineffect_inrect_outrect_outbitmap)">Bitmap::ApplyEffect</a> method. To specify the adjustment, the intensity of the adjustment, and the color channel to which the adjustment applies, pass the address of a <a href="/windows/desktop/api/gdipluseffects/ns-gdipluseffects-colorcurveparams">ColorCurveParams</a> structure to the <a href="/windows/desktop/api/gdipluseffects/nf-gdipluseffects-colorcurve-setparameters">ColorCurve::SetParameters</a> method of a <b>ColorCurve</b> object.