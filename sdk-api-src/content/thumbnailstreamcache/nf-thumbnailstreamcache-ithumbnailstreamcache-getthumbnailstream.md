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

# IThumbnailStreamCache::GetThumbnailStream


## -description


Gets the thumbnail stream. This method is for internal use only and can only be called by the photos application.


## -parameters




### -param path [in]

The path to the thumbnail.


### -param cacheId [in]

The identifier of the thumbnail.


### -param options [in]

The cache options for the thumbnail stream.


### -param requestedThumbnailSize [in]

The requested size of the thumbnail.


### -param thumbnailSize [out]

The actual size of the returned thumbnail.


### -param thumbnailStream [out]

The requested thumbnail.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/9D2C01E7-2B0B-462F-98A3-12ACBC40F6E7">IThumbnailStreamCache</a>
 

 

