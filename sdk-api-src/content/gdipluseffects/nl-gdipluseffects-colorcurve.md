---
UID: NL:gdipluseffects.ColorCurve
title: ColorCurve (gdipluseffects.h)
author: windows-sdk-content
description: The ColorCurve class encompasses eight separate adjustments:\_exposure, density, contrast, highlight, shadow, midtone, white saturation, and black saturation.
old-location: gdiplus\_gdiplus_CLASS_ColorCurve_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\colorcurve.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ColorCurve, ColorCurve class [GDI+], ColorCurve class [GDI+],described, _gdiplus_CLASS_ColorCurve_Class, gdiplus._gdiplus_CLASS_ColorCurve_Class, gdipluseffects/ColorCurve
ms.topic: class
f1_keywords: ["gdipluseffects/ColorCurve"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - gdipluseffects.h
api_name:
 - ColorCurve
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ColorCurve class


## -description


The <b>ColorCurve</b> class encompasses eight separate adjustments: exposure, density, contrast, highlight, shadow, midtone, white saturation, and black saturation. You can apply one of those adjustments to a bitmap by passing the address of a <b>ColorCurve</b> object to the <a href="https://docs.microsoft.com/previous-versions/ms536058(v=vs.85)">Graphics::DrawImage</a> method or to the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-applyeffect(inbitmap_inint_ineffect_inrect_outrect_outbitmap)">Bitmap::ApplyEffect</a> method. To specify the adjustment, the intensity of the adjustment, and the color channel to which the adjustment applies, pass the address of a <a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/ns-gdipluseffects-colorcurveparams">ColorCurveParams</a> structure to the <a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/nf-gdipluseffects-colorcurve-setparameters">ColorCurve::SetParameters</a> method of a <b>ColorCurve</b> object.

