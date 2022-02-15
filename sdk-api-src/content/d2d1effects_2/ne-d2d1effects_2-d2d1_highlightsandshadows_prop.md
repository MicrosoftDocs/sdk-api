---
UID: NE:d2d1effects_2.D2D1_HIGHLIGHTSANDSHADOWS_PROP
title: D2D1_HIGHLIGHTSANDSHADOWS_PROP (d2d1effects_2.h)
description: Identifiers for properties of the Highlights and Shadows effect.
helpviewer_keywords: ["D2D1_HIGHLIGHTSANDSHADOWS_PROP","D2D1_HIGHLIGHTSANDSHADOWS_PROP enumeration [Direct2D]","D2D1_HIGHLIGHTSANDSHADOWS_PROP_CLARITY","D2D1_HIGHLIGHTSANDSHADOWS_PROP_HIGHLIGHTS","D2D1_HIGHLIGHTSANDSHADOWS_PROP_INPUT_GAMMA","D2D1_HIGHLIGHTSANDSHADOWS_PROP_MASK_BLUR_RADIUS","D2D1_HIGHLIGHTSANDSHADOWS_PROP_SHADOWS","d2d1effects_2/D2D1_HIGHLIGHTSANDSHADOWS_PROP","d2d1effects_2/D2D1_HIGHLIGHTSANDSHADOWS_PROP_CLARITY","d2d1effects_2/D2D1_HIGHLIGHTSANDSHADOWS_PROP_HIGHLIGHTS","d2d1effects_2/D2D1_HIGHLIGHTSANDSHADOWS_PROP_INPUT_GAMMA","d2d1effects_2/D2D1_HIGHLIGHTSANDSHADOWS_PROP_MASK_BLUR_RADIUS","d2d1effects_2/D2D1_HIGHLIGHTSANDSHADOWS_PROP_SHADOWS","direct2d.d2d1_highlightsandshadows_prop"]
old-location: direct2d\d2d1_highlightsandshadows_prop.htm
tech.root: Direct2D
ms.assetid: 2E4BACCB-EF29-44FB-8427-C10211BC4899
ms.date: 12/05/2018
ms.keywords: D2D1_HIGHLIGHTSANDSHADOWS_PROP, D2D1_HIGHLIGHTSANDSHADOWS_PROP enumeration [Direct2D], D2D1_HIGHLIGHTSANDSHADOWS_PROP_CLARITY, D2D1_HIGHLIGHTSANDSHADOWS_PROP_HIGHLIGHTS, D2D1_HIGHLIGHTSANDSHADOWS_PROP_INPUT_GAMMA, D2D1_HIGHLIGHTSANDSHADOWS_PROP_MASK_BLUR_RADIUS, D2D1_HIGHLIGHTSANDSHADOWS_PROP_SHADOWS, d2d1effects_2/D2D1_HIGHLIGHTSANDSHADOWS_PROP, d2d1effects_2/D2D1_HIGHLIGHTSANDSHADOWS_PROP_CLARITY, d2d1effects_2/D2D1_HIGHLIGHTSANDSHADOWS_PROP_HIGHLIGHTS, d2d1effects_2/D2D1_HIGHLIGHTSANDSHADOWS_PROP_INPUT_GAMMA, d2d1effects_2/D2D1_HIGHLIGHTSANDSHADOWS_PROP_MASK_BLUR_RADIUS, d2d1effects_2/D2D1_HIGHLIGHTSANDSHADOWS_PROP_SHADOWS, direct2d.d2d1_highlightsandshadows_prop
req.header: d2d1effects_2.h
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
req.typenames: D2D1_HIGHLIGHTSANDSHADOWS_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_HIGHLIGHTSANDSHADOWS_PROP
 - d2d1effects_2/D2D1_HIGHLIGHTSANDSHADOWS_PROP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1effects_2.h
api_name:
 - D2D1_HIGHLIGHTSANDSHADOWS_PROP
---

# D2D1_HIGHLIGHTSANDSHADOWS_PROP enumeration


## -description

Identifiers for properties of the <a href="/windows/desktop/Direct2D/highlights-and-shadows-effect">Highlights and Shadows effect</a>.

## -enum-fields

### -field D2D1_HIGHLIGHTSANDSHADOWS_PROP_HIGHLIGHTS:0

The D2D1_HIGHLIGHTSANDSHADOWS_PROP_HIGHLIGHTS property is a float value indicating how much to increase or decrease highlights.  The allowed range is -1.0 to 1.0. The default value is 0.0.

### -field D2D1_HIGHLIGHTSANDSHADOWS_PROP_SHADOWS:1

The D2D1_HIGHLIGHTSANDSHADOWS_PROP_SHADOWS property is a float value indicating how much to increase or decrease shadows.  The allowed range is -1.0 to 1.0. The default value is 0.0.

### -field D2D1_HIGHLIGHTSANDSHADOWS_PROP_CLARITY:2

The D2D1_HIGHLIGHTSANDSHADOWS_PROP_CLARITY property is a float value indicating how much to increase or decrease clarity.  The allowed range is -1.0 to 1.0. The default value is 0.0.

### -field D2D1_HIGHLIGHTSANDSHADOWS_PROP_INPUT_GAMMA:3

The D2D1_HIGHLIGHTSANDSHADOWS_PROP_INPUT_GAMMA property is a <a href="/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_highlightsandshadows_input_gamma">D2D1_HIGHLIGHTSANDSHADOWS_INPUT_GAMMA</a> enumeration value
          indicating the gamma of the input image.  The Highlights and Shadows effect works in linear gamma space, so if the input image is know to be linear, the D2D1_HIGHLIGHTSANDSHADOWS_INPUT_GAMMA_LINEAR value should be used to prevent sRGB to linear conversions from being performed.

### -field D2D1_HIGHLIGHTSANDSHADOWS_PROP_MASK_BLUR_RADIUS:4

The D2D1_HIGHLIGHTSANDSHADOWS_PROP_MASK_BLUR_RADIUS property is a float value controlling the size of the region used around a pixel to classify the pixel as highlight or shadow. Lower values result in more localized adjustments. 
          The allowed range is 0.0 to 10.0.  The default value is 1.25.

### -field D2D1_HIGHLIGHTSANDSHADOWS_PROP_FORCE_DWORD:0xffffffff
