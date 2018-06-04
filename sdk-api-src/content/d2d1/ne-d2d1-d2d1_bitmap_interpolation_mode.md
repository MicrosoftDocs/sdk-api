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

# D2D1_BITMAP_INTERPOLATION_MODE enumeration


## -description


Specifies the algorithm that is used when images are scaled or rotated.
<div class="alert"><b>Note</b>  Starting in Windows 8, more interpolations modes are available.  See <a href="direct2d.__D2D1_INTERPOLATION_MODE">D2D1_INTERPOLATION_MODE</a> for more info.</div><div> </div>

## -enum-fields




### -field D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR

Use the exact color of the nearest bitmap pixel to the current rendering pixel.


### -field D2D1_BITMAP_INTERPOLATION_MODE_LINEAR

Interpolate a color from the four bitmap pixels that are the nearest to the rendering pixel.


### -field D2D1_BITMAP_INTERPOLATION_MODE_FORCE_DWORD




## -remarks




		To stretch an image, each pixel in the original image must be mapped to a group of pixels in the larger image. To shrink an image, groups of pixels in the original image must be mapped to single pixels in the smaller image. The effectiveness of the algorithms that perform these mappings determines the quality of a scaled image. Algorithms that produce higher-quality scaled images tend to require more processing time. <b>D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR </b>provides faster but lower-quality interpolation, while <b>D2D1_BITMAP_INTERPOLATION_MODE_LINEAR</b> provides higher-quality interpolation.
		
		
		



