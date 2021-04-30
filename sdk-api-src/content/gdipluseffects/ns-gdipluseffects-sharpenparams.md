---
UID: NS:gdipluseffects.SharpenParams
title: SharpenParams (gdipluseffects.h)
description: The SharpenParams structure contains members that specify the nature of a sharpening adjustment to a bitmap.
helpviewer_keywords: ["SharpenParams","SharpenParams structure [GDI+]","_gdiplus_STRUC_SharpenParams","gdiplus._gdiplus_STRUC_SharpenParams","gdipluseffects/SharpenParams"]
old-location: gdiplus\_gdiplus_STRUC_SharpenParams.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\structures\sharpenparams.htm
ms.date: 12/05/2018
ms.keywords: SharpenParams, SharpenParams structure [GDI+], _gdiplus_STRUC_SharpenParams, gdiplus._gdiplus_STRUC_SharpenParams, gdipluseffects/SharpenParams
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
 - SharpenParams
 - gdipluseffects/SharpenParams
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
 - SharpenParams
---

# SharpenParams structure


## -description

The <b>SharpenParams</b> structure contains members that specify the nature of a sharpening adjustment to a bitmap.

You can adjust the sharpness of a bitmap by following these steps. 
<ol>
<li>Create and initialize a <b>SharpenParams</b> structure.</li>
<li>Pass the address of the <b>SharpenParams</b> structure to the <a href="/windows/desktop/api/gdipluseffects/nf-gdipluseffects-sharpen-setparameters">Sharpen::SetParameters</a> method of a <a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-sharpen">Sharpen</a> object.</li>
<li>Pass the address of the <a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-sharpen">Sharpen</a> object to the <a href="/previous-versions/ms536058(v=vs.85)">Graphics::DrawImage</a> method or to the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-applyeffect(inbitmap_inint_ineffect_inrect_outrect_outbitmap)">Bitmap::ApplyEffect</a> method.</li>
</ol>

## -struct-fields

### -field radius

Type: <b>REAL</b>

Real number that specifies the sharpening radius (the radius of the convolution kernel) in pixels. The radius must be in the range 0 through 255. As the radius increases, more surrounding pixels are involved in calculating the new value of a given pixel.

### -field amount

Type: <b>REAL</b>

Real number in the range 0 through 100 that specifies the amount of sharpening to be applied. A value of 0 specifies no sharpening. As the value of <b>amount</b> increases, the sharpness increases.