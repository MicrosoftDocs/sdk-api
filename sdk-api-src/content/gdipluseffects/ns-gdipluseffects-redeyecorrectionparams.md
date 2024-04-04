---
UID: NS:gdipluseffects.RedEyeCorrectionParams
title: RedEyeCorrectionParams (gdipluseffects.h)
description: A RedEyeCorrectionParams structure contains members that specify the areas of a bitmap to which a red-eye correction is applied.
helpviewer_keywords: ["RedEyeCorrectionParams","RedEyeCorrectionParams structure [GDI+]","_gdiplus_STRUC_RedEyeCorrectionParams","gdiplus._gdiplus_STRUC_RedEyeCorrectionParams","gdipluseffects/RedEyeCorrectionParams"]
old-location: gdiplus\_gdiplus_STRUC_RedEyeCorrectionParams.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\structures\redeyecorrectionparams.htm
ms.date: 12/05/2018
ms.keywords: RedEyeCorrectionParams, RedEyeCorrectionParams structure [GDI+], _gdiplus_STRUC_RedEyeCorrectionParams, gdiplus._gdiplus_STRUC_RedEyeCorrectionParams, gdipluseffects/RedEyeCorrectionParams
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
 - RedEyeCorrectionParams
 - gdipluseffects/RedEyeCorrectionParams
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
 - RedEyeCorrectionParams
---

# RedEyeCorrectionParams structure


## -description

A <b>RedEyeCorrectionParams</b> structure contains members that specify the areas of a bitmap to which a red-eye correction is applied.

You can correct red eyes in a bitmap by following these steps.
<ol>
<li>Create and initialize a <b>RedEyeCorrectionParams</b> structure.</li>
<li>Pass the address of the <b>RedEyeCorrectionParams</b> structure to the <a href="/windows/desktop/api/gdipluseffects/nf-gdipluseffects-redeyecorrection-setparameters">RedEyeCorrection::SetParameters</a> method of a <a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-redeyecorrection">RedEyeCorrection</a> object.</li>
<li>Pass the address of the <a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-redeyecorrection">RedEyeCorrection</a> object to the <a href="/previous-versions/ms536058(v=vs.85)">Graphics::DrawImage</a> method or to the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-applyeffect(inbitmap_inint_ineffect_inrect_outrect_outbitmap)">Bitmap::ApplyEffect</a> method.</li>
</ol>

## -struct-fields

### -field numberOfAreas

Type: <b>UINT</b>

Integer that specifies the number of <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structures in the <b>areas</b> array.

### -field areas

Type: <b>RECT*</b>

Pointer to an array of <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structures, each of which specifies an area of the bitmap to which red eye correction should be applied.