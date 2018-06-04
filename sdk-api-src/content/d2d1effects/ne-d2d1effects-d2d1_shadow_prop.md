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



