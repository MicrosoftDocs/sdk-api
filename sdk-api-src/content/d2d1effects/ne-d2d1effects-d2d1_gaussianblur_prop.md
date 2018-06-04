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

# D2D1_GAUSSIANBLUR_PROP enumeration


## -description



          Identifiers for properties of the <a href="https://msdn.microsoft.com/6B8C9A0A-81D6-4CC2-B30B-995D4C2E59FC">Gaussian blur effect</a>.
        


## -enum-fields




### -field D2D1_GAUSSIANBLUR_PROP_STANDARD_DEVIATION


            The amount of blur to be applied to the image. You can compute the blur radius of the kernel by multiplying the standard deviation by 3.
            The units of both the standard deviation and blur radius are DIPs. A value of zero DIPs disables this effect entirely.
            

The type is FLOAT.

The default value is 3.0f.


### -field D2D1_GAUSSIANBLUR_PROP_OPTIMIZATION


            The optimization mode.
            

The type is <a href="https://msdn.microsoft.com/D6A8BB3A-8286-4410-8EA3-A9AEA1797C5E">D2D1_GAUSSIANBLUR_OPTIMIZATION</a>.

The default value is D2D1_GAUSSIANBLUR_OPTIMIZATION_BALANCED.


### -field D2D1_GAUSSIANBLUR_PROP_BORDER_MODE


            The mode used to calculate the border of the image, soft or hard.
            

The type is <a href="https://msdn.microsoft.com/D6A8BB3A-8286-4410-8EA3-A9AEA1797C5E">D2D1_GAUSSIANBLUR_OPTIMIZATION</a>.

The default value is D2D1_BORDER_MODE_SOFT.


### -field D2D1_GAUSSIANBLUR_PROP_FORCE_DWORD



