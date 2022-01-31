---
UID: NE:d2d1effects_2.D2D1_HUETORGB_PROP
title: D2D1_HUETORGB_PROP (d2d1effects_2.h)
description: Identifiers for properties of the Hue to RGB effect.
helpviewer_keywords: ["D2D1_HUETORGB_PROP","D2D1_HUETORGB_PROP enumeration [Direct2D]","D2D1_HUETORGB_PROP_INPUT_COLOR_SPACE","d2d1effects_2/D2D1_HUETORGB_PROP","d2d1effects_2/D2D1_HUETORGB_PROP_INPUT_COLOR_SPACE","direct2d.d2d1_huetorgb_prop"]
old-location: direct2d\d2d1_huetorgb_prop.htm
tech.root: Direct2D
ms.assetid: 293E05B7-DA10-4E71-B519-0AF99EE007EC
ms.date: 12/05/2018
ms.keywords: D2D1_HUETORGB_PROP, D2D1_HUETORGB_PROP enumeration [Direct2D], D2D1_HUETORGB_PROP_INPUT_COLOR_SPACE, d2d1effects_2/D2D1_HUETORGB_PROP, d2d1effects_2/D2D1_HUETORGB_PROP_INPUT_COLOR_SPACE, direct2d.d2d1_huetorgb_prop
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
req.typenames: D2D1_HUETORGB_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_HUETORGB_PROP
 - d2d1effects_2/D2D1_HUETORGB_PROP
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
 - D2D1_HUETORGB_PROP
---

# D2D1_HUETORGB_PROP enumeration


## -description

Identifiers for properties of the <a href="/windows/desktop/Direct2D/hue-to-rgb-effect">Hue to RGB effect</a>.

## -enum-fields

### -field D2D1_HUETORGB_PROP_INPUT_COLOR_SPACE:0

The D2D1_HUETORGB_PROP_INPUT_COLOR_SPACE property is an enumeration value which indicates which color space to convert from. 
          The default value for the property is D2D1_HUETORGB_INPUT_COLOR_SPACE_HUE_SATURATION_VALUE.
          See <a href="/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_huetorgb_input_color_space">D2D1_HUETORGB_INPUT_COLOR_SPACE</a> enumeration for more information.

### -field D2D1_HUETORGB_PROP_FORCE_DWORD:0xffffffff

## -see-also

<a href="/windows/desktop/Direct2D/built-in-effects">Built-in Effects</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect">CreateEffect</a>



<a href="/windows/desktop/Direct2D/hue-to-rgb-effect">Hue to RGB effect</a>
