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

# WICBitmapInterpolationMode enumeration


## -description


Specifies the sampling or filtering mode to use when scaling an image.


## -enum-fields




### -field WICBitmapInterpolationModeNearestNeighbor

A nearest neighbor interpolation algorithm. Also known as nearest pixel or point interpolation.
            

The output pixel is assigned the value of the pixel that the point falls within. No other pixels are considered.


### -field WICBitmapInterpolationModeLinear

A bilinear interpolation algorithm.
            

The output pixel values are computed as a weighted average of the nearest four pixels in a 2x2 grid.


### -field WICBitmapInterpolationModeCubic

A bicubic interpolation algorithm.
            

Destination pixel values are computed as a weighted average of the nearest sixteen pixels in a 4x4 grid. 


### -field WICBitmapInterpolationModeFant

A Fant resampling algorithm.
            

Destination pixel values are computed as a weighted average of the all the pixels that map to the new pixel.


### -field WICBitmapInterpolationModeHighQualityCubic

A high quality bicubic interpolation algorithm. Destination pixel values are computed using a much denser sampling 
      kernel than regular cubic. The kernel is resized in response to the scale factor, making it suitable for downscaling by factors greater than 2.

<div class="alert"><b>Note</b>  This value is supported beginning with Windows 10.</div>
<div> </div>

### -field WICBITMAPINTERPOLATIONMODE_FORCE_DWORD



