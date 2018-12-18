---
UID: NS:d2d1effectauthor.D2D1_RESOURCE_TEXTURE_PROPERTIES
title: D2D1_RESOURCE_TEXTURE_PROPERTIES
author: windows-sdk-content
description: Defines a resource texture when the original resource texture is created.
old-location: direct2d\d2d1_resource_texture_properties.htm
tech.root: direct2d
ms.assetid: 23a524a4-2226-497f-a20b-74cda924c429
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D2D1_RESOURCE_TEXTURE_PROPERTIES, D2D1_RESOURCE_TEXTURE_PROPERTIES structure [Direct2D], d2d1effectauthor/D2D1_RESOURCE_TEXTURE_PROPERTIES, direct2d.d2d1_resource_texture_properties
ms.topic: struct
req.header: d2d1effectauthor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: D2d1.lib; D2d1.dll
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - D2d1.lib
 - D2d1.dll
api_name:
 - D2D1_RESOURCE_TEXTURE_PROPERTIES
product: Windows
targetos: Windows
req.typenames: D2D1_RESOURCE_TEXTURE_PROPERTIES
req.redist: 
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
 

 

