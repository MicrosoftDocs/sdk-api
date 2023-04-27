---
UID: NE:d2d1effects.D2D1_SPOTDIFFUSE_PROP
title: D2D1_SPOTDIFFUSE_PROP (d2d1effects.h)
description: Identifiers for properties of the Spot-diffuse lighting effect.
helpviewer_keywords: ["D2D1_SPOTDIFFUSE_PROP","D2D1_SPOTDIFFUSE_PROP enumeration [Direct2D]","D2D1_SPOTDIFFUSE_PROP_COLOR","D2D1_SPOTDIFFUSE_PROP_DIFFUSE_CONSTANT","D2D1_SPOTDIFFUSE_PROP_FOCUS","D2D1_SPOTDIFFUSE_PROP_KERNEL_UNIT_LENGTH","D2D1_SPOTDIFFUSE_PROP_LIGHT_POSITION","D2D1_SPOTDIFFUSE_PROP_LIMITING_CONE_ANGLE","D2D1_SPOTDIFFUSE_PROP_POINTS_AT","D2D1_SPOTDIFFUSE_PROP_SCALE_MODE","D2D1_SPOTDIFFUSE_PROP_SURFACE_SCALE","d2d1effects/D2D1_SPOTDIFFUSE_PROP","d2d1effects/D2D1_SPOTDIFFUSE_PROP_COLOR","d2d1effects/D2D1_SPOTDIFFUSE_PROP_DIFFUSE_CONSTANT","d2d1effects/D2D1_SPOTDIFFUSE_PROP_FOCUS","d2d1effects/D2D1_SPOTDIFFUSE_PROP_KERNEL_UNIT_LENGTH","d2d1effects/D2D1_SPOTDIFFUSE_PROP_LIGHT_POSITION","d2d1effects/D2D1_SPOTDIFFUSE_PROP_LIMITING_CONE_ANGLE","d2d1effects/D2D1_SPOTDIFFUSE_PROP_POINTS_AT","d2d1effects/D2D1_SPOTDIFFUSE_PROP_SCALE_MODE","d2d1effects/D2D1_SPOTDIFFUSE_PROP_SURFACE_SCALE","direct2d.d2d1_spotdiffuse_prop"]
old-location: direct2d\d2d1_spotdiffuse_prop.htm
tech.root: Direct2D
ms.assetid: 64F7B03C-DD29-4B23-9C8B-2D0390AD61B0
ms.date: 12/05/2018
ms.keywords: D2D1_SPOTDIFFUSE_PROP, D2D1_SPOTDIFFUSE_PROP enumeration [Direct2D], D2D1_SPOTDIFFUSE_PROP_COLOR, D2D1_SPOTDIFFUSE_PROP_DIFFUSE_CONSTANT, D2D1_SPOTDIFFUSE_PROP_FOCUS, D2D1_SPOTDIFFUSE_PROP_KERNEL_UNIT_LENGTH, D2D1_SPOTDIFFUSE_PROP_LIGHT_POSITION, D2D1_SPOTDIFFUSE_PROP_LIMITING_CONE_ANGLE, D2D1_SPOTDIFFUSE_PROP_POINTS_AT, D2D1_SPOTDIFFUSE_PROP_SCALE_MODE, D2D1_SPOTDIFFUSE_PROP_SURFACE_SCALE, d2d1effects/D2D1_SPOTDIFFUSE_PROP, d2d1effects/D2D1_SPOTDIFFUSE_PROP_COLOR, d2d1effects/D2D1_SPOTDIFFUSE_PROP_DIFFUSE_CONSTANT, d2d1effects/D2D1_SPOTDIFFUSE_PROP_FOCUS, d2d1effects/D2D1_SPOTDIFFUSE_PROP_KERNEL_UNIT_LENGTH, d2d1effects/D2D1_SPOTDIFFUSE_PROP_LIGHT_POSITION, d2d1effects/D2D1_SPOTDIFFUSE_PROP_LIMITING_CONE_ANGLE, d2d1effects/D2D1_SPOTDIFFUSE_PROP_POINTS_AT, d2d1effects/D2D1_SPOTDIFFUSE_PROP_SCALE_MODE, d2d1effects/D2D1_SPOTDIFFUSE_PROP_SURFACE_SCALE, direct2d.d2d1_spotdiffuse_prop
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
req.typenames: D2D1_SPOTDIFFUSE_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_SPOTDIFFUSE_PROP
 - d2d1effects/D2D1_SPOTDIFFUSE_PROP
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
 - D2D1_SPOTDIFFUSE_PROP
---

# D2D1_SPOTDIFFUSE_PROP enumeration


## -description

Identifiers for properties of the <a href="/windows/desktop/Direct2D/diffuse-lighting">Spot-diffuse lighting effect</a>.

## -enum-fields

### -field D2D1_SPOTDIFFUSE_PROP_LIGHT_POSITION:0

The light position of the point light source. The property is a D2D1_VECTOR_3F defined as (x, y, z). The units are in device-independent pixels (DIPs) and are unbounded.
            

The type is <a href="/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_3f">D2D1_VECTOR_3F</a>.
            

The default value is {0.0f, 0.0f, 0.0f}.

### -field D2D1_SPOTDIFFUSE_PROP_POINTS_AT:1

Where the spot light is focused. The property is exposed as a D2D1_VECTOR_3F with – (x, y, z). The units are in DIPs and the values are unbounded.
            

The type is <a href="/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_3f">D2D1_VECTOR_3F</a>.
            

The default value is {0.0f, 0.0f, 0.0f}.

### -field D2D1_SPOTDIFFUSE_PROP_FOCUS:2

The focus of the spot light. This property is unitless and is defined between 0 and 200.
            

The type is FLOAT.

The default value is 1.0f.

### -field D2D1_SPOTDIFFUSE_PROP_LIMITING_CONE_ANGLE:3

The cone angle that restricts the region where the light is projected. No light is projected outside the cone. The limiting cone angle is the angle between the spot light axis (the axis between the LightPosition and PointsAt properties) and the spot light cone. This property is defined in degrees and must be between 0 to 90 degrees.
            

The type is FLOAT.

The default value is 90.0f.

### -field D2D1_SPOTDIFFUSE_PROP_DIFFUSE_CONSTANT:4

The ratio of diffuse reflection to amount of incoming light. This property must be between 0 and 10,000 and is unitless.
            

The type is FLOAT.

The default value is 1.0f.

### -field D2D1_SPOTDIFFUSE_PROP_SURFACE_SCALE:5

The scale factor in the Z direction. The surface scale is unitless and must be between 0 and 10,000.
            

The type is FLOAT.

The default value is 1.0f.

### -field D2D1_SPOTDIFFUSE_PROP_COLOR:6

The color of the incoming light. This property is exposed as a Vector 3 – (R, G, B) and used to compute L<sub>R</sub>, L<sub>G</sub>, L<sub>B</sub>.
            

The type is <a href="/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_3f">D2D1_VECTOR_3F</a>.

The default value is {1.0f, 1.0f, 1.0f}

### -field D2D1_SPOTDIFFUSE_PROP_KERNEL_UNIT_LENGTH:7

The size of an element in the Sobel kernel used to generate the surface normal in the X and Y direction. This property maps to the dx and dy values in the Sobel gradient. 
            This property is a <a href="/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_2f">D2D1_VECTOR_2F</a>(Kernel Unit Length X, Kernel Unit Length Y) and is defined in (DIPs/Kernel Unit). 
            The effect uses bilinear interpolation to scale the bitmap to match size of kernel elements.
            

The type is <a href="/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_2f">D2D1_VECTOR_2F</a>.
            

The default value is {1.0f, 1.0f}.

### -field D2D1_SPOTDIFFUSE_PROP_SCALE_MODE:8

The interpolation mode the effect uses to scale the image to the corresponding kernel unit length. There are six scale modes that range in quality and speed.
            

The type is <a href="/windows/desktop/api/d2d1effects/ne-d2d1effects-d2d1_spotdiffuse_scale_mode">D2D1_SPOTDIFFUSE_SCALE_MODE</a>.
            

The default value is D2D1_SPOTDIFFUSE_SCALE_MODE_LINEAR.

### -field D2D1_SPOTDIFFUSE_PROP_FORCE_DWORD:0xffffffff
