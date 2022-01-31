---
UID: NE:d2d1effects.D2D1_TURBULENCE_PROP
title: D2D1_TURBULENCE_PROP (d2d1effects.h)
description: Identifiers for properties of the Turbulence effect.
helpviewer_keywords: ["D2D1_TURBULENCE_PROP","D2D1_TURBULENCE_PROP enumeration [Direct2D]","D2D1_TURBULENCE_PROP_BASE_FREQUENCY","D2D1_TURBULENCE_PROP_NOISE","D2D1_TURBULENCE_PROP_NUM_OCTAVES","D2D1_TURBULENCE_PROP_OFFSET","D2D1_TURBULENCE_PROP_SEED","D2D1_TURBULENCE_PROP_SIZE","D2D1_TURBULENCE_PROP_STITCHABLE","d2d1effects/D2D1_TURBULENCE_PROP","d2d1effects/D2D1_TURBULENCE_PROP_BASE_FREQUENCY","d2d1effects/D2D1_TURBULENCE_PROP_NOISE","d2d1effects/D2D1_TURBULENCE_PROP_NUM_OCTAVES","d2d1effects/D2D1_TURBULENCE_PROP_OFFSET","d2d1effects/D2D1_TURBULENCE_PROP_SEED","d2d1effects/D2D1_TURBULENCE_PROP_SIZE","d2d1effects/D2D1_TURBULENCE_PROP_STITCHABLE","direct2d.d2d1_turbulence_prop"]
old-location: direct2d\d2d1_turbulence_prop.htm
tech.root: Direct2D
ms.assetid: C045CA4D-C6B0-47CD-A479-DC3FDFF8D697
ms.date: 12/05/2018
ms.keywords: D2D1_TURBULENCE_PROP, D2D1_TURBULENCE_PROP enumeration [Direct2D], D2D1_TURBULENCE_PROP_BASE_FREQUENCY, D2D1_TURBULENCE_PROP_NOISE, D2D1_TURBULENCE_PROP_NUM_OCTAVES, D2D1_TURBULENCE_PROP_OFFSET, D2D1_TURBULENCE_PROP_SEED, D2D1_TURBULENCE_PROP_SIZE, D2D1_TURBULENCE_PROP_STITCHABLE, d2d1effects/D2D1_TURBULENCE_PROP, d2d1effects/D2D1_TURBULENCE_PROP_BASE_FREQUENCY, d2d1effects/D2D1_TURBULENCE_PROP_NOISE, d2d1effects/D2D1_TURBULENCE_PROP_NUM_OCTAVES, d2d1effects/D2D1_TURBULENCE_PROP_OFFSET, d2d1effects/D2D1_TURBULENCE_PROP_SEED, d2d1effects/D2D1_TURBULENCE_PROP_SIZE, d2d1effects/D2D1_TURBULENCE_PROP_STITCHABLE, direct2d.d2d1_turbulence_prop
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
req.typenames: D2D1_TURBULENCE_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_TURBULENCE_PROP
 - d2d1effects/D2D1_TURBULENCE_PROP
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
 - D2D1_TURBULENCE_PROP
---

# D2D1_TURBULENCE_PROP enumeration


## -description

Identifiers for properties of the <a href="/windows/desktop/Direct2D/turbulence">Turbulence effect</a>.

## -enum-fields

### -field D2D1_TURBULENCE_PROP_OFFSET:0

The coordinates where the turbulence output is generated.
            

The algorithm used to generate the Perlin noise is position dependent, so a different offset results in a different output.
              This property is not bounded and the units are specified in DIPs.
            

<div class="alert"><b>Note</b>  The offset does not have the same effect as a translation because the noise function output is infinite and the function will wrap around the tile.</div>
<div> </div>
The type is <a href="/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_2f">D2D1_VECTOR_2F</a>.
            

The default value is {0.0f, 0.0f}.

### -field D2D1_TURBULENCE_PROP_SIZE:1

### -field D2D1_TURBULENCE_PROP_BASE_FREQUENCY:2

The base frequencies in the X and Y direction. This property is a float and must be greater than 0. The units are specified in 1/DIPs.
            

A value of 1 (1/DIPs) for the base frequency results in the Perlin noise completing an entire cycle between two pixels. The ease interpolation for these pixels results in completely random pixels, since there is no correlation between the pixels.

A value of 0.1(1/DIPs) for the base frequency, the Perlin noise function repeats every 10 DIPs. This results in correlation between pixels and the typical turbulence effect is visible.

The type is <a href="/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_2f">D2D1_VECTOR_2F</a>.
            

The default value is {0.01f, 0.01f}.

### -field D2D1_TURBULENCE_PROP_NUM_OCTAVES:3

The number of octaves for the noise function. This property is a UINT32 and must be greater than 0.
            

The type is UINT32.

The default value is 1.

### -field D2D1_TURBULENCE_PROP_SEED:4

The seed for the pseudo random generator. This property is unbounded.
            

The type is UINT32.

The default value is 0.

### -field D2D1_TURBULENCE_PROP_NOISE:5

The turbulence noise mode. This property can be either fractal sum or turbulence. Indicates whether to generate a bitmap based on Fractal Noise or the Turbulence function. 
            

The type is <a href="/windows/desktop/api/d2d1effects/ne-d2d1effects-d2d1_turbulence_noise">D2D1_TURBULENCE_NOISE</a>.
            

The default value is D2D1_TURBULENCE_NOISE_FRACTAL_SUM.

### -field D2D1_TURBULENCE_PROP_STITCHABLE:6

Turns stitching on or off. The base frequency is adjusted so that output bitmap can be stitched. This is useful if you want to tile multiple copies of the turbulence effect output.
            

True – The output bitmap can be tiled (using the tile effect) without the appearance of seams. The base frequency is adjusted so that output bitmap can be stitched.

False – The base frequency is not adjusted, so seams may appear between tiles if the bitmap is tiled. 

The type is BOOL.

The default value is FALSE.

### -field D2D1_TURBULENCE_PROP_FORCE_DWORD:0xffffffff
