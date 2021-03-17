---
UID: NS:gdipluseffects.ColorBalanceParams
title: ColorBalanceParams (gdipluseffects.h)
description: A ColorBalanceParams structure contains members that specify the nature of a color balance adjustment.
helpviewer_keywords: ["ColorBalanceParams","ColorBalanceParams structure [GDI+]","_gdiplus_STRUC_ColorBalanceParams","gdiplus._gdiplus_STRUC_ColorBalanceParams","gdipluseffects/ColorBalanceParams"]
old-location: gdiplus\_gdiplus_STRUC_ColorBalanceParams.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\structures\colorbalanceparams.htm
ms.date: 12/05/2018
ms.keywords: ColorBalanceParams, ColorBalanceParams structure [GDI+], _gdiplus_STRUC_ColorBalanceParams, gdiplus._gdiplus_STRUC_ColorBalanceParams, gdipluseffects/ColorBalanceParams
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
 - ColorBalanceParams
 - gdipluseffects/ColorBalanceParams
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
 - ColorBalanceParams
---

# ColorBalanceParams structure


## -description

A <b>ColorBalanceParams</b> structure contains members that specify the nature of a color balance adjustment.

You can change the color balance of a bitmap by following these steps.
<ol>
<li>Create and initialize a <b>ColorBalanceParams</b> structure.</li>
<li>Pass the address of the <b>ColorBalanceParams</b> structure to the <a href="/windows/desktop/api/gdipluseffects/nf-gdipluseffects-colorbalance-setparameters">ColorBalance::SetParameters</a> method of a <a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-colorbalance">ColorBalance</a> object.</li>
<li>Pass the address of the <a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-colorbalance">ColorBalance</a> object to the <a href="/previous-versions/ms536058(v=vs.85)">Graphics::DrawImage</a> method or to the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-applyeffect(inbitmap_inint_ineffect_inrect_outrect_outbitmap)">Bitmap::ApplyEffect</a> method.</li>
</ol>

## -struct-fields

### -field cyanRed

Type: <b>INT</b>

Integer in the range -100 through 100 that specifies a change in the amount of red in the image. If the value is 0, there is no change. As the value moves from 0 to 100, the amount of red in the image increases and the amount of cyan decreases. As the value moves from 0 to -100, the amount of red in the image decreases and the amount of cyan increases.

### -field magentaGreen

Type: <b>INT</b>

Integer in the range -100 through 100 that specifies a change in the amount of green in the image. If the value is 0, there is no change. As the value moves from 0 to 100, the amount of green in the image increases and the amount of magenta decreases. As the value moves from 0 to -100, the amount of green in the image decreases and the amount of magenta increases.

### -field yellowBlue

Type: <b>INT</b>

Integer in the range -100 through 100 that specifies a change in the amount of blue in the image. If the value is 0, there is no change. As the value moves from 0 to 100, the amount of blue in the image increases and the amount of yellow decreases. As the value moves from 0 to -100, the amount of blue in the image decreases and the amount of yellow increases.