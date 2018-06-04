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

# InterpolationMode enumeration


## -description


The <b>InterpolationMode</b> enumeration specifies the algorithm that is used when images are scaled or rotated. This enumeration is used by the <a href="https://msdn.microsoft.com/a9f3b27c-cb16-4d52-9970-ea3708bd1e0c">Graphics::GetInterpolationMode</a> and <a href="https://msdn.microsoft.com/1624691c-fbf0-4d14-8d48-e7c69e0100aa">Graphics::SetInterpolationMode</a> methods of the 
			<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> class.


## -enum-fields




### -field InterpolationModeInvalid

Used internally


### -field InterpolationModeDefault

Specifies the default interpolation mode. 


### -field InterpolationModeLowQuality

Specifies a low-quality mode. 


### -field InterpolationModeHighQuality

Specifies a high-quality mode. 


### -field InterpolationModeBilinear

Specifies bilinear interpolation. No prefiltering is done. This mode is not suitable for shrinking an image below 50 percent of its original size. 


### -field InterpolationModeBicubic

Specifies bicubic interpolation. No prefiltering is done. This mode is not suitable for shrinking an image below 25 percent of its original size. 


### -field InterpolationModeNearestNeighbor

Specifies nearest-neighbor interpolation. 


### -field InterpolationModeHighQualityBilinear

Specifies high-quality, bilinear interpolation. Prefiltering is performed to ensure high-quality shrinking. 


### -field InterpolationModeHighQualityBicubic

Specifies high-quality, bicubic interpolation. Prefiltering is performed to ensure high-quality shrinking. This mode produces the highest quality transformed images. 


## -see-also




<a href="https://msdn.microsoft.com/a9f3b27c-cb16-4d52-9970-ea3708bd1e0c">Graphics::GetInterpolationMode</a>



<a href="https://msdn.microsoft.com/1624691c-fbf0-4d14-8d48-e7c69e0100aa">Graphics::SetInterpolationMode</a>
 

 

