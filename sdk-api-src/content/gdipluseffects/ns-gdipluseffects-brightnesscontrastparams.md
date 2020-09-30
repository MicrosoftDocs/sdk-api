---
UID: NS:gdipluseffects.BrightnessContrastParams
title: BrightnessContrastParams (gdipluseffects.h)
description: A BrightnessContrastParams structure contains members that specify the nature of a brightness or contrast adjustment.
helpviewer_keywords: ["BrightnessContrastParams","BrightnessContrastParams structure [GDI+]","_gdiplus_STRUC_BrightnessContrastParams","gdiplus._gdiplus_STRUC_BrightnessContrastParams","gdipluseffects/BrightnessContrastParams"]
old-location: gdiplus\_gdiplus_STRUC_BrightnessContrastParams.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\structures\brightnesscontrastparams.htm
ms.date: 12/05/2018
ms.keywords: BrightnessContrastParams, BrightnessContrastParams structure [GDI+], _gdiplus_STRUC_BrightnessContrastParams, gdiplus._gdiplus_STRUC_BrightnessContrastParams, gdipluseffects/BrightnessContrastParams
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
 - BrightnessContrastParams
 - gdipluseffects/BrightnessContrastParams
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
 - BrightnessContrastParams
---

# BrightnessContrastParams structure


## -description

A <b>BrightnessContrastParams</b> structure contains members that specify the nature of a brightness or contrast adjustment.

You can change the brightness or contrast (or both) of a bitmap by following these steps.
<ol>
<li>Create and initialize a <b>BrightnessContrastParams</b> structure.</li>
<li>Pass the address of the <b>BrightnessContrastParams</b> structure to the <a href="/windows/desktop/api/gdipluseffects/nf-gdipluseffects-brightnesscontrast-setparameters">BrightnessContrast::SetParameters</a> method of a <a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-brightnesscontrast">BrightnessContrast</a> object.</li>
<li>Pass the address of the <a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-brightnesscontrast">BrightnessContrast</a> object to the <a href="/previous-versions/ms536058(v=vs.85)">Graphics::DrawImage</a> method or to the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-applyeffect(inbitmap_inint_ineffect_inrect_outrect_outbitmap)">Bitmap::ApplyEffect</a> method.</li>
</ol>

## -struct-fields

### -field brightnessLevel

Type: <b>INT</b>

Integer in the range -255 through 255 that specifies the brightness level. If the value is 0, the brightness remains the same. As the value moves from 0 to 255, the brightness of the image increases. As the value moves from 0 to -255, the brightness of the image decreases.

### -field contrastLevel

Type: <b>INT</b>

Integer in the range -100 through 100 that specifies the contrast level. If the value is 0, the contrast remains the same. As the value moves from 0 to 100, the contrast of the image increases. As the value moves from 0 to -100, the contrast of the image decreases.