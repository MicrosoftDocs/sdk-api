---
UID: NF:thumbnailstreamcache.IThumbnailStreamCache.SetThumbnailStream
title: IThumbnailStreamCache::SetThumbnailStream
author: windows-sdk-content
description: Sets the thumbnail stream. This method is for internal use only and can only be called by the photos application.
old-location: shell\ithumbnailstreamcache_setthumbnailstream.htm
tech.root: shell
ms.assetid: F2A105BB-9523-49F1-89B6-57CAF35C1AC4
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: IThumbnailStreamCache interface [Windows Shell],SetThumbnailStream method, IThumbnailStreamCache.SetThumbnailStream, IThumbnailStreamCache::SetThumbnailStream, SetThumbnailStream, SetThumbnailStream method [Windows Shell], SetThumbnailStream method [Windows Shell],IThumbnailStreamCache interface, shell.ithumbnailstreamcache_setthumbnailstream, thumbnailstreamcache/IThumbnailStreamCache::SetThumbnailStream
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: thumbnailstreamcache.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - thumbnailstreamcache.h
api_name:
 - IThumbnailStreamCache.SetThumbnailStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IThumbnailStreamCache::SetThumbnailStream


## -description


Sets the thumbnail stream. This method is for internal use only and can only be called by the photos application.


## -parameters




### -param path [in]

The path to the thumbnail.


### -param cacheId [in]

The identifier of the thumbnail.


### -param thumbnailSize [in]

The size of the thumbnail.


### -param thumbnailStream [in]

The pointer to the thumbnail stream.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/9D2C01E7-2B0B-462F-98A3-12ACBC40F6E7">IThumbnailStreamCache</a>
 

 

