---
UID: NS:gdipluseffects.ColorLUTParams
title: ColorLUTParams (gdipluseffects.h)
description: A ColorLUTParams structure contains members (color lookup tables) that specify color adjustments to a bitmap.
helpviewer_keywords: ["ColorLUTParams","ColorLUTParams structure [GDI+]","_gdiplus_STRUC_ColorLUTParams","gdiplus._gdiplus_STRUC_ColorLUTParams","gdipluseffects/ColorLUTParams"]
old-location: gdiplus\_gdiplus_STRUC_ColorLUTParams.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\structures\colorlutparams.htm
ms.date: 12/05/2018
ms.keywords: ColorLUTParams, ColorLUTParams structure [GDI+], _gdiplus_STRUC_ColorLUTParams, gdiplus._gdiplus_STRUC_ColorLUTParams, gdipluseffects/ColorLUTParams
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
 - ColorLUTParams
 - gdipluseffects/ColorLUTParams
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
 - ColorLUTParams
---

# ColorLUTParams structure


## -description

A <b>ColorLUTParams</b> structure contains members (color lookup tables) that specify color adjustments to a bitmap.

You can apply a custom adjustment to a bitmap by following these steps.
<ol>
<li>Create a <b>ColorLUTParams</b> structure.</li>
<li>Each member of the <b>ColorLUTParams</b> structure is a color lookup table (array of 256 bytes) for a particular color channel, alpha, red, green, or blue. Assign values of your choice to the four lookup tables.</li>
<li>Pass the address of the <b>ColorLUTParams</b> structure to the <a href="/windows/desktop/api/gdipluseffects/nf-gdipluseffects-colorlut-setparameters">ColorLUT::SetParameters</a> method of a <a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-colorlut">ColorLUT</a> object.</li>
<li>Pass the address of the <a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-colorlut">ColorLUT</a> object to the <a href="/previous-versions/ms536058(v=vs.85)">Graphics::DrawImage</a> method or to the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-applyeffect(inbitmap_inint_ineffect_inrect_outrect_outbitmap)">Bitmap::ApplyEffect</a> method.</li>
</ol>

## -struct-fields

### -field lutB

Type: <b>ColorChannelLUT</b>

Array of 256 bytes that specifies the adjustment for the blue channel.

### -field lutG

Type: <b>ColorChannelLUT</b>

Array of 256 bytes that specifies the adjustment for the green channel.

### -field lutR

Type: <b>ColorChannelLUT</b>

Array of 256 bytes that specifies the adjustment for the red channel.

### -field lutA

Type: <b>ColorChannelLUT</b>

Array of 256 bytes that specifies the adjustment for the alpha channel.

## -remarks

A lookup table specifies how existing color channel values should be replaced by new values. A color channel value of j is replaced by the jth entry in the lookup table for that channel. For example, an existing blue channel value of 25 would be replaced by the value of lutB[25].

The ColorChannelLUT data type is defined in GdiplusColorMatrix.h as follows:

<code>typedef BYTE ColorChannelLUT[256];</code>