---
UID: NS:gdipluseffects.LevelsParams
title: LevelsParams (gdipluseffects.h)
description: The LevelsParams structure contains members that specify adjustments to the light, midtone, or dark areas of a bitmap.
helpviewer_keywords: ["LevelsParams","LevelsParams structure [GDI+]","_gdiplus_STRUC_LevelsParams","gdiplus._gdiplus_STRUC_LevelsParams","gdipluseffects/LevelsParams"]
old-location: gdiplus\_gdiplus_STRUC_LevelsParams.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\structures\levelsparams.htm
ms.date: 12/05/2018
ms.keywords: LevelsParams, LevelsParams structure [GDI+], _gdiplus_STRUC_LevelsParams, gdiplus._gdiplus_STRUC_LevelsParams, gdipluseffects/LevelsParams
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
 - LevelsParams
 - gdipluseffects/LevelsParams
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
 - LevelsParams
---

# LevelsParams structure


## -description

The <b>LevelsParams</b> structure contains members that specify adjustments to the light, midtone, or dark areas of a bitmap.

You can adjust the light, midtone, or dark areas of a bitmap by following these steps.
<ol>
<li>Create and initialize a <b>LevelsParams</b> structure.</li>
<li>Pass the address of the <b>LevelsParams</b> structure to the <a href="/windows/desktop/api/gdipluseffects/nf-gdipluseffects-levels-setparameters">Levels::SetParameters</a> method of a <a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-levels">Levels</a> object.</li>
<li>Pass the address of the <a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-levels">Levels</a> object to the <a href="/previous-versions/ms536058(v=vs.85)">Graphics::DrawImage</a> method or to the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-applyeffect(inbitmap_inint_ineffect_inrect_outrect_outbitmap)">Bitmap::ApplyEffect</a> method.</li>
</ol>

## -struct-fields

### -field highlight

Type: <b>INT</b>

Integer in the range 0 through 100 that specifies which pixels should be lightened. You can use this adjustment to lighten pixels that are already lighter than a certain threshold. Setting <b>highlight</b> to 100 specifies no change. Setting <b>highlight</b> to t specifies that a color channel value is increased if it is already greater than t percent of full intensity. For example, setting <b>highlight</b> to 90 specifies that all color channel values greater than 90 percent of full intensity are increased.

### -field midtone

Type: <b>INT</b>

Integer in the range -100 through 100 that specifies how much to lighten or darken an image. Color channel values in the middle of the intensity range are altered more than color channel values near the minimum or maximum intensity. You can use this adjustment to lighten (or darken) an image without loosing the contrast between the darkest and lightest portions of the image. A value of 0 specifies no change. Positive values specify that the midtones are made lighter, and negative values specify that the midtones are made darker.

### -field shadow

Type: <b>INT</b>

Integer in the range 0 through 100 that specifies which pixels should be darkened. You can use this adjustment to darken pixels that are already darker than a certain threshold. Setting <b>shadow</b> to 0 specifies no change. Setting <b>shadow</b> to t specifies that a color channel value is decreased if it is already less than t percent of full intensity. For example, setting <b>shadow</b> to 10 specifies that all color channel values less than 10 percent of full intensity are decreased.