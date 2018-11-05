---
UID: NE:d2d1effects.D2D1_SHADOW_PROP
title: D2D1_SHADOW_PROP
author: windows-sdk-content
description: Identifiers for properties of the Shadow effect.
old-location: direct2d\d2d1_shadow_prop.htm
tech.root: direct2d
ms.assetid: 332B5743-D702-4DBC-8482-FEAD43641C3A
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: D2D1_SHADOW_PROP, D2D1_SHADOW_PROP enumeration [Direct2D], D2D1_SHADOW_PROP_BLUR_STANDARD_DEVIATION, D2D1_SHADOW_PROP_COLOR, D2D1_SHADOW_PROP_OPTIMIZATION, d2d1effects/D2D1_SHADOW_PROP, d2d1effects/D2D1_SHADOW_PROP_BLUR_STANDARD_DEVIATION, d2d1effects/D2D1_SHADOW_PROP_COLOR, d2d1effects/D2D1_SHADOW_PROP_OPTIMIZATION, direct2d.d2d1_shadow_prop
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
 - D2D1_SHADOW_PROP
product: Windows
targetos: Windows
req.typenames: D2D1_SHADOW_PROP
req.redist: 
---

# D2D1_SHADOW_PROP enumeration


## -description


Identifiers for properties of the <a href="https://msdn.microsoft.com/53525584-10CF-46C2-9400-C4FB225D4693">Shadow effect</a>.
        


## -enum-fields




### -field D2D1_SHADOW_PROP_BLUR_STANDARD_DEVIATION

The amount of blur to be applied to the alpha channel of the image. You can compute the blur radius of the kernel by multiplying the standard deviation by 3.
            The units of both the standard deviation and blur radius are DIPs.
            

This property is the same as the Gaussian Blur standard deviation property.

The type is FLOAT.

The default value is 3.0f.


### -field D2D1_SHADOW_PROP_COLOR

The color of the drop shadow. This property is a D2D1_VECTOR_4F defined as: (R, G, B, A). You must specify this color in straight alpha.
            

The type is <a href="https://msdn.microsoft.com/6D931285-0F2B-44BE-8A1A-2348AC49A8DF">D2D1_VECTOR_4F</a>.

The default value is {0.0f, 0.0f, 0.0f, 1.0f}.


### -field D2D1_SHADOW_PROP_OPTIMIZATION

The level of performance optimization.
            

The type is <a href="https://msdn.microsoft.com/1C509608-BEBA-4E4C-8EC5-88B587D81B34">D2D1_SHADOW_OPTIMIZATION</a>.

The default value is D2D1_SHADOW_OPTIMIZATION_BALANCED.


### -field D2D1_SHADOW_PROP_FORCE_DWORD



