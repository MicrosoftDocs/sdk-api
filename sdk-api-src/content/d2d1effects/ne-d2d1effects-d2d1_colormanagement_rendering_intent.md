---
UID: NE:d2d1effects.D2D1_COLORMANAGEMENT_RENDERING_INTENT
title: D2D1_COLORMANAGEMENT_RENDERING_INTENT (d2d1effects.h)
description: Specifies which ICC rendering intent the Color management effect should use.
helpviewer_keywords: ["D2D1_COLORMANAGEMENT_RENDERING_INTENT","D2D1_COLORMANAGEMENT_RENDERING_INTENT enumeration [Direct2D]","D2D1_COLORMANAGEMENT_RENDERING_INTENT_ABSOLUTE_COLORIMETRIC","D2D1_COLORMANAGEMENT_RENDERING_INTENT_PERCEPTUAL","D2D1_COLORMANAGEMENT_RENDERING_INTENT_RELATIVE_COLORIMETRIC","D2D1_COLORMANAGEMENT_RENDERING_INTENT_SATURATION","d2d1effects/D2D1_COLORMANAGEMENT_RENDERING_INTENT","d2d1effects/D2D1_COLORMANAGEMENT_RENDERING_INTENT_ABSOLUTE_COLORIMETRIC","d2d1effects/D2D1_COLORMANAGEMENT_RENDERING_INTENT_PERCEPTUAL","d2d1effects/D2D1_COLORMANAGEMENT_RENDERING_INTENT_RELATIVE_COLORIMETRIC","d2d1effects/D2D1_COLORMANAGEMENT_RENDERING_INTENT_SATURATION","direct2d.d2d1_colormanagement_rendering_intent"]
old-location: direct2d\d2d1_colormanagement_rendering_intent.htm
tech.root: Direct2D
ms.assetid: 64161335-7974-4B8D-9385-045A94625FE1
ms.date: 12/05/2018
ms.keywords: D2D1_COLORMANAGEMENT_RENDERING_INTENT, D2D1_COLORMANAGEMENT_RENDERING_INTENT enumeration [Direct2D], D2D1_COLORMANAGEMENT_RENDERING_INTENT_ABSOLUTE_COLORIMETRIC, D2D1_COLORMANAGEMENT_RENDERING_INTENT_PERCEPTUAL, D2D1_COLORMANAGEMENT_RENDERING_INTENT_RELATIVE_COLORIMETRIC, D2D1_COLORMANAGEMENT_RENDERING_INTENT_SATURATION, d2d1effects/D2D1_COLORMANAGEMENT_RENDERING_INTENT, d2d1effects/D2D1_COLORMANAGEMENT_RENDERING_INTENT_ABSOLUTE_COLORIMETRIC, d2d1effects/D2D1_COLORMANAGEMENT_RENDERING_INTENT_PERCEPTUAL, d2d1effects/D2D1_COLORMANAGEMENT_RENDERING_INTENT_RELATIVE_COLORIMETRIC, d2d1effects/D2D1_COLORMANAGEMENT_RENDERING_INTENT_SATURATION, direct2d.d2d1_colormanagement_rendering_intent
req.header: d2d1effects.h
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
req.typenames: D2D1_COLORMANAGEMENT_RENDERING_INTENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_COLORMANAGEMENT_RENDERING_INTENT
 - d2d1effects/D2D1_COLORMANAGEMENT_RENDERING_INTENT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1effects.h
api_name:
 - D2D1_COLORMANAGEMENT_RENDERING_INTENT
---

# D2D1_COLORMANAGEMENT_RENDERING_INTENT enumeration


## -description

Specifies which ICC rendering intent the <a href="/windows/desktop/Direct2D/color-management">Color management effect</a> should use.

## -enum-fields

### -field D2D1_COLORMANAGEMENT_RENDERING_INTENT_PERCEPTUAL:0

The effect compresses or expands the full color gamut of the image to fill the color gamut of the device, 
          so that gray balance is preserved but colorimetric accuracy may not be preserved.

### -field D2D1_COLORMANAGEMENT_RENDERING_INTENT_RELATIVE_COLORIMETRIC:1

The effect preserves the chroma of colors in the image at the possible expense of hue and lightness.

### -field D2D1_COLORMANAGEMENT_RENDERING_INTENT_SATURATION:2

The effect adjusts colors that fall outside the range of colors the output device renders to the closest color available. It does not preserve the white point.

### -field D2D1_COLORMANAGEMENT_RENDERING_INTENT_ABSOLUTE_COLORIMETRIC:3

The effect adjusts any colors that fall outside the range that the output device can render to the closest color that can be rendered. The effect does not change the other colors and preserves the white point.

### -field D2D1_COLORMANAGEMENT_RENDERING_INTENT_FORCE_DWORD:0xffffffff
