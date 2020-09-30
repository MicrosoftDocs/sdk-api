---
UID: NS:gdipluseffects.TintParams
title: TintParams (gdipluseffects.h)
description: A TintParams structure contains members that specify the nature of a tint adjustment to a bitmap.
helpviewer_keywords: ["TintParams","TintParams structure [GDI+]","_gdiplus_STRUC_TintParams","gdiplus._gdiplus_STRUC_TintParams","gdipluseffects/TintParams"]
old-location: gdiplus\_gdiplus_STRUC_TintParams.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\structures\tintparams.htm
ms.date: 12/05/2018
ms.keywords: TintParams, TintParams structure [GDI+], _gdiplus_STRUC_TintParams, gdiplus._gdiplus_STRUC_TintParams, gdipluseffects/TintParams
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
 - TintParams
 - gdipluseffects/TintParams
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
 - TintParams
---

# TintParams structure


## -description

A <b>TintParams</b> structure contains members that specify the nature of a tint adjustment to a bitmap.

You can adjust the tint of a bitmap by following these steps.
<ol>
<li>Create and initialize a <b>TintParams</b> structure.</li>
<li>Pass the address of the <b>TintParams</b> structure to the <a href="/windows/desktop/api/gdipluseffects/nf-gdipluseffects-tint-setparameters">Tint::SetParameters</a> method of a <a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-tint">Tint</a> object.</li>
<li>Pass the address of the <a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-tint">Tint</a> object to the <a href="/previous-versions/ms536058(v=vs.85)">Graphics::DrawImage</a> method or to the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-applyeffect(inbitmap_inint_ineffect_inrect_outrect_outbitmap)">Bitmap::ApplyEffect</a> method.</li>
</ol>

## -struct-fields

### -field hue

Type: <b>INT</b>

Integer in the range -180 through 180 that specifies the hue to be strengthened or weakened. A value of 0 specifies blue. A positive value specifies a clockwise angle on the color wheel. For example, positive 60 specifies cyan and positive 120 specifies green. A negative value specifies a counter-clockwise angle on the color wheel. For example, negative 60 specifies magenta and negative 120 specifies red.

### -field amount

Type: <b>INT</b>

Integer in the range -100 through 100 that specifies how much the hue (given by the <b>hue</b> parameter) is strengthened or weakened. A value of 0 specifies no change. Positive values specify that the hue is strengthened and negative values specify that the hue is weakened.