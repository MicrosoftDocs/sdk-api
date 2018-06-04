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

# D2D1_RESOURCE_TEXTURE_PROPERTIES structure


## -description


Defines a resource texture when the original resource texture is created.


## -struct-fields




### -field extents

The extents of the resource table in each dimension.


### -field dimensions

The number of dimensions in the resource texture. This must be a number from 1 to 3.


### -field bufferPrecision

The precision of the resource texture to create. 


### -field channelDepth

The number of channels in the resource texture.


### -field filter

The filtering mode to use on the texture.


### -field extendModes

Specifies how pixel values beyond the extent of the texture will be sampled, in every dimension.


## -see-also




<a href="https://msdn.microsoft.com/265888DA-03C2-42F0-92D8-FEB542F9BAA4">ID2D1EffectContext::CreateResourceTexture</a>
 

 

