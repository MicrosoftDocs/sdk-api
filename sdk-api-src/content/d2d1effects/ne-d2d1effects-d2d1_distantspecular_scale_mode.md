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

# D2D1_DISTANTSPECULAR_SCALE_MODE enumeration


## -description


The interpolation mode the <a href="https://msdn.microsoft.com/74D71A2D-8D1D-4FDE-898A-2D2F5A8D5D31">Distant-specular lighting effect</a> uses to scale the image to the corresponding kernel unit length. 
        There are six scale modes that range in quality and speed.


## -enum-fields




### -field D2D1_DISTANTSPECULAR_SCALE_MODE_NEAREST_NEIGHBOR

Samples the nearest single point and uses that. This mode uses less processing time, but outputs the lowest quality image.


### -field D2D1_DISTANTSPECULAR_SCALE_MODE_LINEAR

Uses a four point sample and linear interpolation. This mode outputs a higher quality image than nearest neighbor.


### -field D2D1_DISTANTSPECULAR_SCALE_MODE_CUBIC

Uses a 16 sample cubic kernel for interpolation. This mode uses the most processing time, but outputs a higher quality image.


### -field D2D1_DISTANTSPECULAR_SCALE_MODE_MULTI_SAMPLE_LINEAR

Uses 4 linear samples within a single pixel for good edge anti-aliasing. This mode is good for scaling down by small amounts on images with few pixels.


### -field D2D1_DISTANTSPECULAR_SCALE_MODE_ANISOTROPIC

Uses anisotropic filtering to sample a pattern according to the transformed shape of the bitmap.


### -field D2D1_DISTANTSPECULAR_SCALE_MODE_HIGH_QUALITY_CUBIC

Uses a variable size high quality cubic kernel to perform a pre-downscale the image if downscaling is involved in the transform matrix. 
          Then uses the cubic interpolation mode for the final output.


### -field D2D1_DISTANTSPECULAR_SCALE_MODE_FORCE_DWORD



