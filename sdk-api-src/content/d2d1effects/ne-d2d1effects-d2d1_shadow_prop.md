---
UID: NE:d2d1effects.D2D1_SHADOW_PROP
title: D2D1_SHADOW_PROP (d2d1effects.h)
description: Identifiers for properties of the Shadow effect.
helpviewer_keywords: ["D2D1_SHADOW_PROP","D2D1_SHADOW_PROP enumeration [Direct2D]","D2D1_SHADOW_PROP_BLUR_STANDARD_DEVIATION","D2D1_SHADOW_PROP_COLOR","D2D1_SHADOW_PROP_OPTIMIZATION","d2d1effects/D2D1_SHADOW_PROP","d2d1effects/D2D1_SHADOW_PROP_BLUR_STANDARD_DEVIATION","d2d1effects/D2D1_SHADOW_PROP_COLOR","d2d1effects/D2D1_SHADOW_PROP_OPTIMIZATION","direct2d.d2d1_shadow_prop"]
old-location: direct2d\d2d1_shadow_prop.htm
tech.root: Direct2D
ms.assetid: 332B5743-D702-4DBC-8482-FEAD43641C3A
ms.date: 12/05/2018
ms.keywords: D2D1_SHADOW_PROP, D2D1_SHADOW_PROP enumeration [Direct2D], D2D1_SHADOW_PROP_BLUR_STANDARD_DEVIATION, D2D1_SHADOW_PROP_COLOR, D2D1_SHADOW_PROP_OPTIMIZATION, d2d1effects/D2D1_SHADOW_PROP, d2d1effects/D2D1_SHADOW_PROP_BLUR_STANDARD_DEVIATION, d2d1effects/D2D1_SHADOW_PROP_COLOR, d2d1effects/D2D1_SHADOW_PROP_OPTIMIZATION, direct2d.d2d1_shadow_prop
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
req.typenames: D2D1_SHADOW_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_SHADOW_PROP
 - d2d1effects/D2D1_SHADOW_PROP
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
 - D2D1_SHADOW_PROP
---

# D2D1_SHADOW_PROP enumeration


## -description

Identifiers for properties of the <a href="/windows/desktop/Direct2D/drop-shadow">Shadow effect</a>.

## -enum-fields

### -field D2D1_SHADOW_PROP_BLUR_STANDARD_DEVIATION:0

The amount of blur to be applied to the alpha channel of the image. You can compute the blur radius of the kernel by multiplying the standard deviation by 3.
            The units of both the standard deviation and blur radius are DIPs.
            

This property is the same as the Gaussian Blur standard deviation property.

The type is FLOAT.

The default value is 3.0f.

### -field D2D1_SHADOW_PROP_COLOR:1

The color of the drop shadow. This property is a D2D1_VECTOR_4F defined as: (R, G, B, A). You must specify this color in straight alpha.
            

The type is <a href="/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_4f">D2D1_VECTOR_4F</a>.

The default value is {0.0f, 0.0f, 0.0f, 1.0f}.

### -field D2D1_SHADOW_PROP_OPTIMIZATION:2

The level of performance optimization.
            

The type is <a href="/windows/desktop/api/d2d1effects/ne-d2d1effects-d2d1_shadow_optimization">D2D1_SHADOW_OPTIMIZATION</a>.

The default value is D2D1_SHADOW_OPTIMIZATION_BALANCED.

### -field D2D1_SHADOW_PROP_FORCE_DWORD:0xffffffff
