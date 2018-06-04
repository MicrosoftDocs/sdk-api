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

# _DXVA2_VideoLighting enumeration


## -description


Describes the intended lighting conditions for viewing video content. These flags are used in the <a href="https://msdn.microsoft.com/eba2c56b-8951-4dc5-91ae-1371793ce787">DXVA2_ExtendedFormat</a> structure.


## -enum-fields




### -field DXVA2_VideoLightingMask

Bitmask to validate flag values. This value is not a valid flag.


### -field DXVA2_VideoLighting_Unknown

Unknown. Treat as DXVA2_VideoLighting_dim.


### -field DXVA2_VideoLighting_bright

Outdoor lighting.


### -field DXVA2_VideoLighting_office

Medium brightness; for example, an office.


### -field DXVA2_VideoLighting_dim

Dim; for example, a living room with a television and some additional low lighting.


### -field DXVA2_VideoLighting_dark

Dark; for example, a movie theater.


## -remarks



This enumeration is equivalent to the <b>DXVA_VideoLighting</b> enumeration used in DXVA 1.0.

If you are using the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface to describe the video format, the video lighting is specified in the <a href="https://msdn.microsoft.com/697590e3-898e-4ac9-8390-7b0994b6e571">MF_MT_VIDEO_LIGHTING</a> attribute.




## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

