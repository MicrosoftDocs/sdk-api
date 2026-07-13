---
UID: NF:thumbnailstreamcache.IThumbnailStreamCache.SetThumbnailStream
title: IThumbnailStreamCache::SetThumbnailStream (thumbnailstreamcache.h)
description: Sets the thumbnail stream. This method is for internal use only and can only be called by the photos application.
helpviewer_keywords: ["IThumbnailStreamCache interface [Windows Shell]","SetThumbnailStream method","IThumbnailStreamCache.SetThumbnailStream","IThumbnailStreamCache::SetThumbnailStream","SetThumbnailStream","SetThumbnailStream method [Windows Shell]","SetThumbnailStream method [Windows Shell]","IThumbnailStreamCache interface","shell.ithumbnailstreamcache_setthumbnailstream","thumbnailstreamcache/IThumbnailStreamCache::SetThumbnailStream"]
old-location: shell\ithumbnailstreamcache_setthumbnailstream.htm
tech.root: shell
ms.assetid: F2A105BB-9523-49F1-89B6-57CAF35C1AC4
ms.date: 12/05/2018
ms.keywords: IThumbnailStreamCache interface [Windows Shell],SetThumbnailStream method, IThumbnailStreamCache.SetThumbnailStream, IThumbnailStreamCache::SetThumbnailStream, SetThumbnailStream, SetThumbnailStream method [Windows Shell], SetThumbnailStream method [Windows Shell],IThumbnailStreamCache interface, shell.ithumbnailstreamcache_setthumbnailstream, thumbnailstreamcache/IThumbnailStreamCache::SetThumbnailStream
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IThumbnailStreamCache::SetThumbnailStream
 - thumbnailstreamcache/IThumbnailStreamCache::SetThumbnailStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - thumbnailstreamcache.h
api_name:
 - IThumbnailStreamCache.SetThumbnailStream
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

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/thumbnailstreamcache/nn-thumbnailstreamcache-ithumbnailstreamcache">IThumbnailStreamCache</a>