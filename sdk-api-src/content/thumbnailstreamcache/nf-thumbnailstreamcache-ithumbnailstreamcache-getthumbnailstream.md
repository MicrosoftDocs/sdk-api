---
UID: NF:thumbnailstreamcache.IThumbnailStreamCache.GetThumbnailStream
title: IThumbnailStreamCache::GetThumbnailStream (thumbnailstreamcache.h)
description: Gets the thumbnail stream. This method is for internal use only and can only be called by the photos application.
helpviewer_keywords: ["GetThumbnailStream","GetThumbnailStream method [Windows Shell]","GetThumbnailStream method [Windows Shell]","IThumbnailStreamCache interface","IThumbnailStreamCache interface [Windows Shell]","GetThumbnailStream method","IThumbnailStreamCache.GetThumbnailStream","IThumbnailStreamCache::GetThumbnailStream","shell.ithumbnailstreamcache_getthumbnailstream","thumbnailstreamcache/IThumbnailStreamCache::GetThumbnailStream"]
old-location: shell\ithumbnailstreamcache_getthumbnailstream.htm
tech.root: shell
ms.assetid: 66A89AF9-DEBE-485C-B8E9-519F63386F7D
ms.date: 12/05/2018
ms.keywords: GetThumbnailStream, GetThumbnailStream method [Windows Shell], GetThumbnailStream method [Windows Shell],IThumbnailStreamCache interface, IThumbnailStreamCache interface [Windows Shell],GetThumbnailStream method, IThumbnailStreamCache.GetThumbnailStream, IThumbnailStreamCache::GetThumbnailStream, shell.ithumbnailstreamcache_getthumbnailstream, thumbnailstreamcache/IThumbnailStreamCache::GetThumbnailStream
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
 - IThumbnailStreamCache::GetThumbnailStream
 - thumbnailstreamcache/IThumbnailStreamCache::GetThumbnailStream
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
 - IThumbnailStreamCache.GetThumbnailStream
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

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/thumbnailstreamcache/nn-thumbnailstreamcache-ithumbnailstreamcache">IThumbnailStreamCache</a>