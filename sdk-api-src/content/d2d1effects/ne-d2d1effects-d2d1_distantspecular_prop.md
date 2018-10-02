---
UID: NE:d2d1effects.D2D1_DISTANTSPECULAR_PROP
title: D2D1_DISTANTSPECULAR_PROP
author: windows-sdk-content
description: Identifiers for properties of the Distant-specular lighting effect.
old-location: direct2d\d2d1_distantspecular_prop.htm
tech.root: direct2d
ms.assetid: 66C00620-4209-4837-9305-4B1B1148881A
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: D2D1_DISTANTSPECULAR_PROP, D2D1_DISTANTSPECULAR_PROP enumeration [Direct2D], D2D1_DISTANTSPECULAR_PROP_AZIMUTH, D2D1_DISTANTSPECULAR_PROP_COLOR, D2D1_DISTANTSPECULAR_PROP_ELEVATION, D2D1_DISTANTSPECULAR_PROP_KERNEL_UNIT_LENGTH, D2D1_DISTANTSPECULAR_PROP_SCALE_MODE, D2D1_DISTANTSPECULAR_PROP_SPECULAR_CONSTANT, D2D1_DISTANTSPECULAR_PROP_SPECULAR_EXPONENT, D2D1_DISTANTSPECULAR_PROP_SURFACE_SCALE, d2d1effects/D2D1_DISTANTSPECULAR_PROP, d2d1effects/D2D1_DISTANTSPECULAR_PROP_AZIMUTH, d2d1effects/D2D1_DISTANTSPECULAR_PROP_COLOR, d2d1effects/D2D1_DISTANTSPECULAR_PROP_ELEVATION, d2d1effects/D2D1_DISTANTSPECULAR_PROP_KERNEL_UNIT_LENGTH, d2d1effects/D2D1_DISTANTSPECULAR_PROP_SCALE_MODE, d2d1effects/D2D1_DISTANTSPECULAR_PROP_SPECULAR_CONSTANT, d2d1effects/D2D1_DISTANTSPECULAR_PROP_SPECULAR_EXPONENT, d2d1effects/D2D1_DISTANTSPECULAR_PROP_SURFACE_SCALE, direct2d.d2d1_distantspecular_prop
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1effects.h
api_name:
 - D2D1_DISTANTSPECULAR_PROP
product: Windows
targetos: Windows
req.typenames: D2D1_DISTANTSPECULAR_PROP
req.redist: 
---

# D2D1_DISTANTSPECULAR_PROP enumeration


## -description


Identifiers for properties of the <a href="https://msdn.microsoft.com/en-us/library/Hh706332(v=VS.85).aspx">Distant-specular lighting effect</a>.
        


## -enum-fields




### -field D2D1_DISTANTSPECULAR_PROP_AZIMUTH

The direction angle of the light source in the XY plane relative to the X-axis in the counter clock wise direction. The units are in degrees and must be between 0 and 360 degrees.
            

The type is FLOAT.

The default value is 0.0f.


### -field D2D1_DISTANTSPECULAR_PROP_ELEVATION

The direction angle of the light source in the YZ plane relative to the Y-axis in the counter clock wise direction. The units are in degrees and must be between 0 and 360 degrees.
            

The type is FLOAT.

The default value is 0.0f.


### -field D2D1_DISTANTSPECULAR_PROP_SPECULAR_EXPONENT

The exponent for the specular term in the Phong lighting equation. A larger value corresponds to a more reflective surface. The value is unitless and must be between 1.0 and 128.
            

The type is FLOAT.

The default value is 1.0f.


### -field D2D1_DISTANTSPECULAR_PROP_SPECULAR_CONSTANT

The ratio of specular reflection to the incoming light. The value is unitless and must be between 0 and 10,000.
            

The type is FLOAT.

The default value is 1.0f.


### -field D2D1_DISTANTSPECULAR_PROP_SURFACE_SCALE

The scale factor in the Z direction. The value is unitless and must be between 0 and 10,000.
            

The type is FLOAT.

The default value is 1.0f.


### -field D2D1_DISTANTSPECULAR_PROP_COLOR

The color of the incoming light. This property is exposed as a D2D1_VECTOR_3F – (R, G, B) and used to compute LR, LG, LB.
            

The type is D2D1_VECTOR_3F.

The default value is {1.0f, 1.0f, 1.0f}.


### -field D2D1_DISTANTSPECULAR_PROP_KERNEL_UNIT_LENGTH

The size of an element in the Sobel kernel used to generate the surface normal in the X and Y direction. This property is a D2D1_VECTOR_2F (Kernel Unit Length X, Kernel Unit Length Y) and is defined in (device-independent pixels (DIPs)/Kernel Unit). The effect uses bilinear interpolation to scale the bitmap to match size of kernel elements.
            

The type is D2D1_VECTOR_2F.

The default value is {1.0f, 1.0f}.


### -field D2D1_DISTANTSPECULAR_PROP_SCALE_MODE

The interpolation mode the effect uses to scale the image to the corresponding kernel unit length. There are six scale modes that range in quality and speed.
            

The type is D2D1_DISTANTSPECULAR_SCALE_MODE.

The default value is D2D1_DISTANTSPECULAR_SCALE_MODE_LINEAR.


### -field D2D1_DISTANTSPECULAR_PROP_FORCE_DWORD



