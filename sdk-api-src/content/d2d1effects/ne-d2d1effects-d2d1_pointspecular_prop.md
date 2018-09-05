---
UID: NE:d2d1effects.D2D1_POINTSPECULAR_PROP
title: D2D1_POINTSPECULAR_PROP
author: windows-sdk-content
description: Identifiers for properties of the Point-specular lighting effect.
old-location: direct2d\d2d1_pointspecular_prop.htm
old-project: direct2d
ms.assetid: 5026F106-F5AA-4D03-BEFE-F1E8E880EF44
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: D2D1_POINTSPECULAR_PROP, D2D1_POINTSPECULAR_PROP enumeration [Direct2D], D2D1_POINTSPECULAR_PROP_COLOR, D2D1_POINTSPECULAR_PROP_KERNEL_UNIT_LENGTH, D2D1_POINTSPECULAR_PROP_LIGHT_POSITION, D2D1_POINTSPECULAR_PROP_SCALE_MODE, D2D1_POINTSPECULAR_PROP_SPECULAR_CONSTANT, D2D1_POINTSPECULAR_PROP_SPECULAR_EXPONENT, D2D1_POINTSPECULAR_PROP_SURFACE_SCALE, d2d1effects/D2D1_POINTSPECULAR_PROP, d2d1effects/D2D1_POINTSPECULAR_PROP_COLOR, d2d1effects/D2D1_POINTSPECULAR_PROP_KERNEL_UNIT_LENGTH, d2d1effects/D2D1_POINTSPECULAR_PROP_LIGHT_POSITION, d2d1effects/D2D1_POINTSPECULAR_PROP_SCALE_MODE, d2d1effects/D2D1_POINTSPECULAR_PROP_SPECULAR_CONSTANT, d2d1effects/D2D1_POINTSPECULAR_PROP_SPECULAR_EXPONENT, d2d1effects/D2D1_POINTSPECULAR_PROP_SURFACE_SCALE, direct2d.d2d1_pointspecular_prop
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d2d1effects.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D2D1_POINTSPECULAR_PROP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1effects.h
api_name:
 - D2D1_POINTSPECULAR_PROP
product: Windows
targetos: Windows
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
---

# D2D1_POINTSPECULAR_PROP enumeration


## -description


Identifiers for properties of the <a href="https://msdn.microsoft.com/89E22FD0-BB7F-465F-A79C-056CA9F14F5D">Point-specular lighting effect</a>.
        


## -enum-fields




### -field D2D1_POINTSPECULAR_PROP_LIGHT_POSITION

The light position of the point light source. The property is a D2D1_VECTOR_3F defined as (x, y, z). The units are in device-independent pixels (DIPs) and the values are unitless and unbounded.
            

The type is D2D1_VECTOR_3F.

The default value is {0.0f, 0.0f, 0.0f}.


### -field D2D1_POINTSPECULAR_PROP_SPECULAR_EXPONENT

The exponent for the specular term in the Phong lighting equation. A larger value corresponds to a more reflective surface. This value is unitless and must be between 1.0 and 128.
            

The type is FLOAT.

The default value is 1.0f.


### -field D2D1_POINTSPECULAR_PROP_SPECULAR_CONSTANT

The ratio of specular reflection to the incoming light. The value is unitless and must be between 0 and 10,000.
            

The type is FLOAT.

The default value is 1.0f.


### -field D2D1_POINTSPECULAR_PROP_SURFACE_SCALE

The scale factor in the Z direction for generating a height map. The value is unitless and must be between 0 and 10,000.
            

The type is FLOAT.

The default value is 1.0f.


### -field D2D1_POINTSPECULAR_PROP_COLOR

The color of the incoming light. This property is exposed as a <a href="https://msdn.microsoft.com/469A4FFC-6B5B-4C88-B6A5-23AFD41B885A">D2D1_VECTOR_3F</a> – (R, G, B) and used to compute LR, LG, LB.
            

The type is <a href="https://msdn.microsoft.com/469A4FFC-6B5B-4C88-B6A5-23AFD41B885A">D2D1_VECTOR_3F</a>.

The default value is {1.0f, 1.0f, 1.0f}.


### -field D2D1_POINTSPECULAR_PROP_KERNEL_UNIT_LENGTH

The size of an element in the Sobel kernel used to generate the surface normal in the X and Y directions. This property maps to the dx and dy values in the Sobel gradient. 
            This property is a <a href="https://msdn.microsoft.com/DD180090-D2F4-4DF3-8652-101713C01AE4">D2D1_VECTOR_2F</a>(Kernel Unit Length X, Kernel Unit Length Y) and is defined in (DIPs/Kernel Unit). 
            The effect uses bilinear interpolation to scale the bitmap to match size of kernel elements.
            

The type is <a href="https://msdn.microsoft.com/DD180090-D2F4-4DF3-8652-101713C01AE4">D2D1_VECTOR_2F</a>.

The default value is {1.0f, 1.0f}.


### -field D2D1_POINTSPECULAR_PROP_SCALE_MODE

The interpolation mode the effect uses to scale the image to the corresponding kernel unit length. There are six scale modes that range in quality and speed.
            

The type is <a href="https://msdn.microsoft.com/8583C25C-DB30-42FC-B158-2479110647FD">D2D1_POINTSPECULAR_SCALE_MODE</a>.

The default value is D2D1_POINTSPECULAR_SCALE_MODE_LINEAR.


### -field D2D1_POINTSPECULAR_PROP_FORCE_DWORD



