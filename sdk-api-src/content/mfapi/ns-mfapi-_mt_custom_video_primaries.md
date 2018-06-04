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

# _MT_CUSTOM_VIDEO_PRIMARIES structure


## -description



Defines custom color primaries for a video source. The color primaries define how to convert colors from RGB color space to CIE XYZ color space.




## -struct-fields




### -field fRx

Red x-coordinate.


### -field fRy

Red y-coordinate.


### -field fGx

Green x-coordinate.


### -field fGy

Green y-coordinate.


### -field fBx

Blue x-coordinate.


### -field fBy

Blue y-coordinate.


### -field fWx

White point x-coordinate.


### -field fWy

White point y-coordinate.


## -remarks



This structure is used with the <a href="https://msdn.microsoft.com/dc5df755-53cf-4910-af42-309f1f46b1ed">MF_MT_CUSTOM_VIDEO_PRIMARIES</a> attribute.




## -see-also




<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

