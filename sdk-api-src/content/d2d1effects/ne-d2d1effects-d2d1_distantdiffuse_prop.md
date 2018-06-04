---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# D2D1_DISTANTDIFFUSE_PROP enumeration


## -description


Identifiers for properties of the <a href="https://msdn.microsoft.com/981FD58B-0565-4D0E-957C-3ED81BA8A6EB">Distant-diffuse lighting effect</a>.


## -enum-fields




### -field D2D1_DISTANTDIFFUSE_PROP_AZIMUTH

The direction angle of the light source in the XY plane relative to the X-axis in the counter clock wise direction. The units are in degrees and must be between 0 and 360 degrees.
            

The type is FLOAT.

The default value is 0.0f.


### -field D2D1_DISTANTDIFFUSE_PROP_ELEVATION

The direction angle of the light source in the YZ plane relative to the Y-axis in the counter clock wise direction. The units are in degrees and must be between 0 and 360 degrees. 
            

The type is FLOAT.

The default value is 0.0f.


### -field D2D1_DISTANTDIFFUSE_PROP_DIFFUSE_CONSTANT

The ratio of diffuse reflection to amount of incoming light. This property must be between 0 and 10,000 and is unitless. 
            

The type is FLOAT.

The default value is 1.0f.


### -field D2D1_DISTANTDIFFUSE_PROP_SURFACE_SCALE

The scale factor in the Z direction. The surface scale is unitless and must be between 0 and 10,000.
            

The type is FLOAT.

The default value is 1.0f.


### -field D2D1_DISTANTDIFFUSE_PROP_COLOR

The color of the incoming light. This property is exposed as a D2D1_VECTOR_3F – (R, G, B) and used to compute LR, LG, LB. 
            

The type is D2D1_VECTOR_3F.

The default value is {1.0f, 1.0f, 1.0f}.


### -field D2D1_DISTANTDIFFUSE_PROP_KERNEL_UNIT_LENGTH

The size of an element in the Sobel kernel used to generate the surface normal in the X and Y direction. This property maps to the dx and dy values in the Sobel gradient. This property is a D2D1_VECTOR_2F (Kernel Unit Length X, Kernel Unit Length Y) and is defined in (device-independent pixels (DIPs)/Kernel Unit). The effect uses bilinear interpolation to scale the bitmap to match size of kernel elements. 
            

The type is D2D1_VECTOR_2F.

The default value is {1.0f, 1.0f}.


### -field D2D1_DISTANTDIFFUSE_PROP_SCALE_MODE

The interpolation mode the effect uses to scale the image to the corresponding kernel unit length. There are six scale modes that range in quality and speed.
            

The type is D2D1_DISTANTDIFFUSE_SCALE_MODE.

The default value is D2D1_DISTANTDIFFUSE_SCALE_MODE_LINEAR.


### -field D2D1_DISTANTDIFFUSE_PROP_FORCE_DWORD



