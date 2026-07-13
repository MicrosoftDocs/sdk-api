---
UID: NE:d2d1effects.D2D1_POINTSPECULAR_PROP
title: D2D1_POINTSPECULAR_PROP (d2d1effects.h)
description: Identifiers for properties of the Point-specular lighting effect.
helpviewer_keywords: ["D2D1_POINTSPECULAR_PROP","D2D1_POINTSPECULAR_PROP enumeration [Direct2D]","D2D1_POINTSPECULAR_PROP_COLOR","D2D1_POINTSPECULAR_PROP_KERNEL_UNIT_LENGTH","D2D1_POINTSPECULAR_PROP_LIGHT_POSITION","D2D1_POINTSPECULAR_PROP_SCALE_MODE","D2D1_POINTSPECULAR_PROP_SPECULAR_CONSTANT","D2D1_POINTSPECULAR_PROP_SPECULAR_EXPONENT","D2D1_POINTSPECULAR_PROP_SURFACE_SCALE","d2d1effects/D2D1_POINTSPECULAR_PROP","d2d1effects/D2D1_POINTSPECULAR_PROP_COLOR","d2d1effects/D2D1_POINTSPECULAR_PROP_KERNEL_UNIT_LENGTH","d2d1effects/D2D1_POINTSPECULAR_PROP_LIGHT_POSITION","d2d1effects/D2D1_POINTSPECULAR_PROP_SCALE_MODE","d2d1effects/D2D1_POINTSPECULAR_PROP_SPECULAR_CONSTANT","d2d1effects/D2D1_POINTSPECULAR_PROP_SPECULAR_EXPONENT","d2d1effects/D2D1_POINTSPECULAR_PROP_SURFACE_SCALE","direct2d.d2d1_pointspecular_prop"]
old-location: direct2d\d2d1_pointspecular_prop.htm
tech.root: Direct2D
ms.assetid: 5026F106-F5AA-4D03-BEFE-F1E8E880EF44
ms.date: 12/05/2018
ms.keywords: D2D1_POINTSPECULAR_PROP, D2D1_POINTSPECULAR_PROP enumeration [Direct2D], D2D1_POINTSPECULAR_PROP_COLOR, D2D1_POINTSPECULAR_PROP_KERNEL_UNIT_LENGTH, D2D1_POINTSPECULAR_PROP_LIGHT_POSITION, D2D1_POINTSPECULAR_PROP_SCALE_MODE, D2D1_POINTSPECULAR_PROP_SPECULAR_CONSTANT, D2D1_POINTSPECULAR_PROP_SPECULAR_EXPONENT, D2D1_POINTSPECULAR_PROP_SURFACE_SCALE, d2d1effects/D2D1_POINTSPECULAR_PROP, d2d1effects/D2D1_POINTSPECULAR_PROP_COLOR, d2d1effects/D2D1_POINTSPECULAR_PROP_KERNEL_UNIT_LENGTH, d2d1effects/D2D1_POINTSPECULAR_PROP_LIGHT_POSITION, d2d1effects/D2D1_POINTSPECULAR_PROP_SCALE_MODE, d2d1effects/D2D1_POINTSPECULAR_PROP_SPECULAR_CONSTANT, d2d1effects/D2D1_POINTSPECULAR_PROP_SPECULAR_EXPONENT, d2d1effects/D2D1_POINTSPECULAR_PROP_SURFACE_SCALE, direct2d.d2d1_pointspecular_prop
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
req.typenames: D2D1_POINTSPECULAR_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_POINTSPECULAR_PROP
 - d2d1effects/D2D1_POINTSPECULAR_PROP
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
 - D2D1_POINTSPECULAR_PROP
---

# D2D1_POINTSPECULAR_PROP enumeration


## -description

Identifiers for properties of the <a href="/windows/desktop/Direct2D/point-specular">Point-specular lighting effect</a>.

## -enum-fields

### -field D2D1_POINTSPECULAR_PROP_LIGHT_POSITION:0

The light position of the point light source. The property is a D2D1_VECTOR_3F defined as (x, y, z). The units are in device-independent pixels (DIPs) and the values are unitless and unbounded.
            

The type is D2D1_VECTOR_3F.

The default value is {0.0f, 0.0f, 0.0f}.

### -field D2D1_POINTSPECULAR_PROP_SPECULAR_EXPONENT:1

The exponent for the specular term in the Phong lighting equation. A larger value corresponds to a more reflective surface. This value is unitless and must be between 1.0 and 128.
            

The type is FLOAT.

The default value is 1.0f.

### -field D2D1_POINTSPECULAR_PROP_SPECULAR_CONSTANT:2

The ratio of specular reflection to the incoming light. The value is unitless and must be between 0 and 10,000.
            

The type is FLOAT.

The default value is 1.0f.

### -field D2D1_POINTSPECULAR_PROP_SURFACE_SCALE:3

The scale factor in the Z direction for generating a height map. The value is unitless and must be between 0 and 10,000.
            

The type is FLOAT.

The default value is 1.0f.

### -field D2D1_POINTSPECULAR_PROP_COLOR:4

The color of the incoming light. This property is exposed as a <a href="/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_3f">D2D1_VECTOR_3F</a> – (R, G, B) and used to compute LR, LG, LB.
            

The type is <a href="/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_3f">D2D1_VECTOR_3F</a>.

The default value is {1.0f, 1.0f, 1.0f}.

### -field D2D1_POINTSPECULAR_PROP_KERNEL_UNIT_LENGTH:5

The size of an element in the Sobel kernel used to generate the surface normal in the X and Y directions. This property maps to the dx and dy values in the Sobel gradient. 
            This property is a <a href="/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_2f">D2D1_VECTOR_2F</a>(Kernel Unit Length X, Kernel Unit Length Y) and is defined in (DIPs/Kernel Unit). 
            The effect uses bilinear interpolation to scale the bitmap to match size of kernel elements.
            

The type is <a href="/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_2f">D2D1_VECTOR_2F</a>.

The default value is {1.0f, 1.0f}.

### -field D2D1_POINTSPECULAR_PROP_SCALE_MODE:6

The interpolation mode the effect uses to scale the image to the corresponding kernel unit length. There are six scale modes that range in quality and speed.
            

The type is <a href="/windows/desktop/api/d2d1effects/ne-d2d1effects-d2d1_pointspecular_scale_mode">D2D1_POINTSPECULAR_SCALE_MODE</a>.

The default value is D2D1_POINTSPECULAR_SCALE_MODE_LINEAR.

### -field D2D1_POINTSPECULAR_PROP_FORCE_DWORD:0xffffffff
