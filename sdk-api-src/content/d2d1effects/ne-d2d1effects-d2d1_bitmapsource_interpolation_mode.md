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

# D2D1_BITMAPSOURCE_INTERPOLATION_MODE enumeration


## -description


The interpolation mode used to scale the image in the <a href="https://msdn.microsoft.com/86646111-208A-4E6D-A28C-7B23A1742D24">Bitmap source effect</a>.
        If the mode disables the mipmap, then BitmapSouce will cache the image at the resolution determined by the Scale and EnableDPICorrection properties.
      


## -enum-fields




### -field D2D1_BITMAPSOURCE_INTERPOLATION_MODE_NEAREST_NEIGHBOR

Samples the nearest single point and uses that. Doesn't generate a mipmap. 


### -field D2D1_BITMAPSOURCE_INTERPOLATION_MODE_LINEAR

Uses a four point sample and linear interpolation. Doesn't generate a mipmap. 


### -field D2D1_BITMAPSOURCE_INTERPOLATION_MODE_CUBIC

Uses a 16 sample cubic kernel for interpolation. Doesn't generate a mipmap. 


### -field D2D1_BITMAPSOURCE_INTERPOLATION_MODE_FANT

Uses the WIC fant interpolation, the same as the IWICBitmapScaler interface. Doesn't generate a mipmap.


### -field D2D1_BITMAPSOURCE_INTERPOLATION_MODE_MIPMAP_LINEAR

Generates mipmap chain in system memory using bilinear interpolation. For each mipmap the effect scales to the nearest multiple of 0.5 using bilinear interpolation 
          and then scales the remaining amount using linear interpolation.


### -field D2D1_BITMAPSOURCE_INTERPOLATION_MODE_FORCE_DWORD



