---
UID: NS:gdipluseffects.ColorCurveParams
title: ColorCurveParams (gdipluseffects.h)
description: A ColorCurveParams structure contains members that specify an adjustment to the colors of a bitmap.
helpviewer_keywords: ["ColorCurveParams","ColorCurveParams structure [GDI+]","_gdiplus_STRUC_ColorCurveParams","gdiplus._gdiplus_STRUC_ColorCurveParams","gdipluseffects/ColorCurveParams"]
old-location: gdiplus\_gdiplus_STRUC_ColorCurveParams.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\structures\colorcurveparams.htm
ms.date: 12/05/2018
ms.keywords: ColorCurveParams, ColorCurveParams structure [GDI+], _gdiplus_STRUC_ColorCurveParams, gdiplus._gdiplus_STRUC_ColorCurveParams, gdipluseffects/ColorCurveParams
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
 - ColorCurveParams
 - gdipluseffects/ColorCurveParams
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
 - ColorCurveParams
---

# ColorCurveParams structure


## -description

A <b>ColorCurveParams</b> structure contains members that specify an adjustment to the colors of a bitmap.

The <a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-colorcurve">ColorCurve</a> class encompasses eight separate adjustments: exposure, density, contrast, highlight, shadow, midtone, white saturation, and black saturation. You can apply one of those adjustments to a bitmap by following these steps.
<ol>
<li>Create and initialize a <b>ColorCurveParams</b> structure.</li>
<li>Pass the address of the <b>ColorCurveParams</b> structure to the <a href="/windows/desktop/api/gdipluseffects/nf-gdipluseffects-colorcurve-setparameters">ColorCurve::SetParameters</a> method of a <a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-colorcurve">ColorCurve</a> object.</li>
<li>Pass the address of the <a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-colorcurve">ColorCurve</a> object to the <a href="/previous-versions/ms536058(v=vs.85)">Graphics::DrawImage</a> method or to the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-applyeffect(inbitmap_inint_ineffect_inrect_outrect_outbitmap)">Bitmap::ApplyEffect</a> method.</li>
</ol>

## -struct-fields

### -field adjustment

Type: <b><a href="/windows/desktop/api/gdipluseffects/ne-gdipluseffects-curveadjustments">CurveAdjustments</a></b>

Element of the <a href="/windows/desktop/api/gdipluseffects/ne-gdipluseffects-curveadjustments">CurveAdjustments</a> enumeration that specifies the adjustment to be applied.

### -field channel

Type: <b><a href="/windows/desktop/api/gdipluseffects/ne-gdipluseffects-curvechannel">CurveChannel</a></b>

Element of the <a href="/windows/desktop/api/gdipluseffects/ne-gdipluseffects-curvechannel">CurveChannel</a> enumeration that specifies the color channel to which the adjustment applies.

### -field adjustValue

Type: <b>INT</b>

Integer that specifies the intensity of the adjustment. The range of acceptable values depends on which adjustment is being applied. To see the range of acceptable values for a particular adjustment, see the <a href="/windows/desktop/api/gdipluseffects/ne-gdipluseffects-curveadjustments">CurveAdjustments</a> enumeration.