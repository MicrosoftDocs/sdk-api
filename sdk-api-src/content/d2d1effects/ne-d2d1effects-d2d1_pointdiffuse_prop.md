---
UID: NE:d2d1effects.D2D1_POINTDIFFUSE_PROP
title: D2D1_POINTDIFFUSE_PROP
author: windows-sdk-content
description: Identifiers for properties of the Point-diffuse lighting effect.
old-location: direct2d\d2d1_pointdiffuse_prop.htm
tech.root: direct2d
ms.assetid: D5FD5E6E-A50C-4434-9F68-F0B41E79267A
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: D2D1_POINTDIFFUSE_PROP, D2D1_POINTDIFFUSE_PROP enumeration [Direct2D], D2D1_POINTDIFFUSE_PROP_COLOR, D2D1_POINTDIFFUSE_PROP_DIFFUSE_CONSTANT, D2D1_POINTDIFFUSE_PROP_KERNEL_UNIT_LENGTH, D2D1_POINTDIFFUSE_PROP_LIGHT_POSITION, D2D1_POINTDIFFUSE_PROP_SCALE_MODE, D2D1_POINTDIFFUSE_PROP_SURFACE_SCALE, d2d1effects/D2D1_POINTDIFFUSE_PROP, d2d1effects/D2D1_POINTDIFFUSE_PROP_COLOR, d2d1effects/D2D1_POINTDIFFUSE_PROP_DIFFUSE_CONSTANT, d2d1effects/D2D1_POINTDIFFUSE_PROP_KERNEL_UNIT_LENGTH, d2d1effects/D2D1_POINTDIFFUSE_PROP_LIGHT_POSITION, d2d1effects/D2D1_POINTDIFFUSE_PROP_SCALE_MODE, d2d1effects/D2D1_POINTDIFFUSE_PROP_SURFACE_SCALE, direct2d.d2d1_pointdiffuse_prop
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
 - D2D1_POINTDIFFUSE_PROP
product: Windows
targetos: Windows
req.typenames: D2D1_POINTDIFFUSE_PROP
req.redist: 
---

# D2D1_POINTDIFFUSE_PROP enumeration


## -description


Identifiers for properties of the <a href="https://msdn.microsoft.com/C98A4962-B9EB-4095-9AC4-F1C32C574892">Point-diffuse lighting effect</a>.
        


## -enum-fields




### -field D2D1_POINTDIFFUSE_PROP_LIGHT_POSITION

The light position of the point light source. The property is a D2D1_VECTOR_3F defined as (x, y, z). The units are in device-independent pixels (DIPs) and are unbounded.
            

The type is <a href="https://msdn.microsoft.com/469A4FFC-6B5B-4C88-B6A5-23AFD41B885A">D2D1_VECTOR_3F</a>.

The default value is {0.0f, 0.0f, 0.0f}.


### -field D2D1_POINTDIFFUSE_PROP_DIFFUSE_CONSTANT

The ratio of diffuse reflection to amount of incoming light. This property must be between 0 and 10,000 and is unitless.
            

The type is FLOAT.

The default value is 1.0f.


### -field D2D1_POINTDIFFUSE_PROP_SURFACE_SCALE

The scale factor in the Z direction. The surface scale is unitless and must be between 0 and 10,000.
            

The type is FLOAT.

The default value is 1.0f.


### -field D2D1_POINTDIFFUSE_PROP_COLOR

The color of the incoming light. This property is exposed as a Vector 3 – (R, G, B) and used to compute LR, LG, LB.
            

The type is <a href="https://msdn.microsoft.com/469A4FFC-6B5B-4C88-B6A5-23AFD41B885A">D2D1_VECTOR_3F</a>.

The default value is {1.0f, 1.0f, 1.0f}.


### -field D2D1_POINTDIFFUSE_PROP_KERNEL_UNIT_LENGTH

The size of an element in the Sobel kernel used to generate the surface normal in the X and Y direction. This property maps to the dx and dy values in the Sobel gradient. 
            This property is a <a href="https://msdn.microsoft.com/DD180090-D2F4-4DF3-8652-101713C01AE4">D2D1_VECTOR_2F</a> (Kernel Unit Length X, Kernel Unit Length Y) and is defined in (DIPs/Kernel Unit). 
            The effect uses bilinear interpolation to scale the bitmap to match size of kernel elements.
            

The type is <a href="https://msdn.microsoft.com/DD180090-D2F4-4DF3-8652-101713C01AE4">D2D1_VECTOR_2F</a>.

The default value is {1.0f, 1.0f}.


### -field D2D1_POINTDIFFUSE_PROP_SCALE_MODE

The interpolation mode the effect uses to scale the image to the corresponding kernel unit length. There are six scale modes that range in quality and speed.
            

The type is <a href="https://msdn.microsoft.com/552CCE58-0D79-468C-831D-EBEFE2F87F95">D2D1_POINTDIFFUSE_SCALE_MODE</a>.

The default value is D2D1_POINTDIFFUSE_SCALE_MODE_LINEAR.


### -field D2D1_POINTDIFFUSE_PROP_FORCE_DWORD



