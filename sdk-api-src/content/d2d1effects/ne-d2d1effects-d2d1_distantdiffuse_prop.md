---
UID: NE:d2d1effects.D2D1_DISTANTDIFFUSE_PROP
title: D2D1_DISTANTDIFFUSE_PROP (d2d1effects.h)
description: Identifiers for properties of the Distant-diffuse lighting effect.
helpviewer_keywords: ["D2D1_DISTANTDIFFUSE_PROP","D2D1_DISTANTDIFFUSE_PROP enumeration [Direct2D]","D2D1_DISTANTDIFFUSE_PROP_AZIMUTH","D2D1_DISTANTDIFFUSE_PROP_COLOR","D2D1_DISTANTDIFFUSE_PROP_DIFFUSE_CONSTANT","D2D1_DISTANTDIFFUSE_PROP_ELEVATION","D2D1_DISTANTDIFFUSE_PROP_KERNEL_UNIT_LENGTH","D2D1_DISTANTDIFFUSE_PROP_SCALE_MODE","D2D1_DISTANTDIFFUSE_PROP_SURFACE_SCALE","d2d1effects/D2D1_DISTANTDIFFUSE_PROP","d2d1effects/D2D1_DISTANTDIFFUSE_PROP_AZIMUTH","d2d1effects/D2D1_DISTANTDIFFUSE_PROP_COLOR","d2d1effects/D2D1_DISTANTDIFFUSE_PROP_DIFFUSE_CONSTANT","d2d1effects/D2D1_DISTANTDIFFUSE_PROP_ELEVATION","d2d1effects/D2D1_DISTANTDIFFUSE_PROP_KERNEL_UNIT_LENGTH","d2d1effects/D2D1_DISTANTDIFFUSE_PROP_SCALE_MODE","d2d1effects/D2D1_DISTANTDIFFUSE_PROP_SURFACE_SCALE","direct2d.d2d1_distantdiffuse_prop"]
old-location: direct2d\d2d1_distantdiffuse_prop.htm
tech.root: Direct2D
ms.assetid: C47029DF-D612-4256-ABFC-57F42614E78A
ms.date: 12/05/2018
ms.keywords: D2D1_DISTANTDIFFUSE_PROP, D2D1_DISTANTDIFFUSE_PROP enumeration [Direct2D], D2D1_DISTANTDIFFUSE_PROP_AZIMUTH, D2D1_DISTANTDIFFUSE_PROP_COLOR, D2D1_DISTANTDIFFUSE_PROP_DIFFUSE_CONSTANT, D2D1_DISTANTDIFFUSE_PROP_ELEVATION, D2D1_DISTANTDIFFUSE_PROP_KERNEL_UNIT_LENGTH, D2D1_DISTANTDIFFUSE_PROP_SCALE_MODE, D2D1_DISTANTDIFFUSE_PROP_SURFACE_SCALE, d2d1effects/D2D1_DISTANTDIFFUSE_PROP, d2d1effects/D2D1_DISTANTDIFFUSE_PROP_AZIMUTH, d2d1effects/D2D1_DISTANTDIFFUSE_PROP_COLOR, d2d1effects/D2D1_DISTANTDIFFUSE_PROP_DIFFUSE_CONSTANT, d2d1effects/D2D1_DISTANTDIFFUSE_PROP_ELEVATION, d2d1effects/D2D1_DISTANTDIFFUSE_PROP_KERNEL_UNIT_LENGTH, d2d1effects/D2D1_DISTANTDIFFUSE_PROP_SCALE_MODE, d2d1effects/D2D1_DISTANTDIFFUSE_PROP_SURFACE_SCALE, direct2d.d2d1_distantdiffuse_prop
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
req.typenames: D2D1_DISTANTDIFFUSE_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_DISTANTDIFFUSE_PROP
 - d2d1effects/D2D1_DISTANTDIFFUSE_PROP
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
 - D2D1_DISTANTDIFFUSE_PROP
---

# D2D1_DISTANTDIFFUSE_PROP enumeration


## -description

Identifiers for properties of the <a href="/windows/desktop/Direct2D/distant-diffuse">Distant-diffuse lighting effect</a>.

## -enum-fields

### -field D2D1_DISTANTDIFFUSE_PROP_AZIMUTH:0

The direction angle of the light source in the XY plane relative to the X-axis in the counter clock wise direction. The units are in degrees and must be between 0 and 360 degrees.
            

The type is FLOAT.

The default value is 0.0f.

### -field D2D1_DISTANTDIFFUSE_PROP_ELEVATION:1

The direction angle of the light source in the YZ plane relative to the Y-axis in the counter clock wise direction. The units are in degrees and must be between 0 and 360 degrees. 
            

The type is FLOAT.

The default value is 0.0f.

### -field D2D1_DISTANTDIFFUSE_PROP_DIFFUSE_CONSTANT:2

The ratio of diffuse reflection to amount of incoming light. This property must be between 0 and 10,000 and is unitless. 
            

The type is FLOAT.

The default value is 1.0f.

### -field D2D1_DISTANTDIFFUSE_PROP_SURFACE_SCALE:3

The scale factor in the Z direction. The surface scale is unitless and must be between 0 and 10,000.
            

The type is FLOAT.

The default value is 1.0f.

### -field D2D1_DISTANTDIFFUSE_PROP_COLOR:4

The color of the incoming light. This property is exposed as a D2D1_VECTOR_3F – (R, G, B) and used to compute LR, LG, LB. 
            

The type is D2D1_VECTOR_3F.

The default value is {1.0f, 1.0f, 1.0f}.

### -field D2D1_DISTANTDIFFUSE_PROP_KERNEL_UNIT_LENGTH:5

The size of an element in the Sobel kernel used to generate the surface normal in the X and Y direction. This property maps to the dx and dy values in the Sobel gradient. This property is a D2D1_VECTOR_2F (Kernel Unit Length X, Kernel Unit Length Y) and is defined in (device-independent pixels (DIPs)/Kernel Unit). The effect uses bilinear interpolation to scale the bitmap to match size of kernel elements. 
            

The type is D2D1_VECTOR_2F.

The default value is {1.0f, 1.0f}.

### -field D2D1_DISTANTDIFFUSE_PROP_SCALE_MODE:6

The interpolation mode the effect uses to scale the image to the corresponding kernel unit length. There are six scale modes that range in quality and speed.
            

The type is D2D1_DISTANTDIFFUSE_SCALE_MODE.

The default value is D2D1_DISTANTDIFFUSE_SCALE_MODE_LINEAR.

### -field D2D1_DISTANTDIFFUSE_PROP_FORCE_DWORD:0xffffffff
