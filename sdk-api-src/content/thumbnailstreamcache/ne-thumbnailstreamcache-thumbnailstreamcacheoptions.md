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

# ThumbnailStreamCacheOptions enumeration


## -description


Defines the cache options used by the <a href="https://msdn.microsoft.com/9D2C01E7-2B0B-462F-98A3-12ACBC40F6E7">IThumbnailStreamCache</a> interface.


## -enum-fields




### -field ExtractIfNotCached

Return the cached thumbnail if it is already cached, otherwise extract the thumbnail to the cache.


### -field ReturnOnlyIfCached

Return the thumbnail only if it is already cached.


### -field ResizeThumbnail

Resize the thumbnail to match the requested size.


### -field AllowSmallerSize

Can return a cached thumbnail that is smaller than the requested size.


## -see-also




<a href="https://msdn.microsoft.com/9D2C01E7-2B0B-462F-98A3-12ACBC40F6E7">IThumbnailStreamCache</a>
 

 

