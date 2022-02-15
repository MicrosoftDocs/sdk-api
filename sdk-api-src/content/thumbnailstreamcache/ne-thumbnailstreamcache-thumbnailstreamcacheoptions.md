---
UID: NE:thumbnailstreamcache.ThumbnailStreamCacheOptions
title: ThumbnailStreamCacheOptions (thumbnailstreamcache.h)
description: Defines the cache options used by the IThumbnailStreamCache interface.
helpviewer_keywords: ["AllowSmallerSize","ExtractIfNotCached","ResizeThumbnail","ReturnOnlyIfCached","ThumbnailStreamCacheOptions","ThumbnailStreamCacheOptions enumeration [Windows Shell]","shell.thumbnailstreamcacheoptions","thumbnailstreamcache/AllowSmallerSize","thumbnailstreamcache/ExtractIfNotCached","thumbnailstreamcache/ResizeThumbnail","thumbnailstreamcache/ReturnOnlyIfCached","thumbnailstreamcache/ThumbnailStreamCacheOptions"]
old-location: shell\thumbnailstreamcacheoptions.htm
tech.root: shell
ms.assetid: E148138E-E41F-4274-B40A-7BF49BCF2AB4
ms.date: 12/05/2018
ms.keywords: AllowSmallerSize, ExtractIfNotCached, ResizeThumbnail, ReturnOnlyIfCached, ThumbnailStreamCacheOptions, ThumbnailStreamCacheOptions enumeration [Windows Shell], shell.thumbnailstreamcacheoptions, thumbnailstreamcache/AllowSmallerSize, thumbnailstreamcache/ExtractIfNotCached, thumbnailstreamcache/ResizeThumbnail, thumbnailstreamcache/ReturnOnlyIfCached, thumbnailstreamcache/ThumbnailStreamCacheOptions
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
req.typenames: ThumbnailStreamCacheOptions
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ThumbnailStreamCacheOptions
 - thumbnailstreamcache/ThumbnailStreamCacheOptions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - thumbnailstreamcache.h
api_name:
 - ThumbnailStreamCacheOptions
---

# ThumbnailStreamCacheOptions enumeration


## -description

Defines the cache options used by the <a href="/windows/desktop/api/thumbnailstreamcache/nn-thumbnailstreamcache-ithumbnailstreamcache">IThumbnailStreamCache</a> interface.

## -enum-fields

### -field ExtractIfNotCached:0

Return the cached thumbnail if it is already cached, otherwise extract the thumbnail to the cache.

### -field ReturnOnlyIfCached:0x1

Return the thumbnail only if it is already cached.

### -field ResizeThumbnail:0x2

Resize the thumbnail to match the requested size.

### -field AllowSmallerSize:0x4

Can return a cached thumbnail that is smaller than the requested size.

## -see-also

<a href="/windows/desktop/api/thumbnailstreamcache/nn-thumbnailstreamcache-ithumbnailstreamcache">IThumbnailStreamCache</a>
