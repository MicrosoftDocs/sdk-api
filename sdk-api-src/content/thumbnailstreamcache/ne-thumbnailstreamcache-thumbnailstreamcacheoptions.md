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
f1_keywords:
- thumbnailstreamcache/ThumbnailStreamCacheOptions
dev_langs:
- c++
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
- HeaderDef
api_location:
- thumbnailstreamcache.h
api_name:
- ThumbnailStreamCacheOptions
targetos: Windows
req.typenames: ThumbnailStreamCacheOptions
req.redist: 
ms.custom: 19H1
---

# ThumbnailStreamCacheOptions enumeration


## -description


Defines the cache options used by the <a href="https://docs.microsoft.com/windows/desktop/api/thumbnailstreamcache/nn-thumbnailstreamcache-ithumbnailstreamcache">IThumbnailStreamCache</a> interface.


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




<a href="https://docs.microsoft.com/windows/desktop/api/thumbnailstreamcache/nn-thumbnailstreamcache-ithumbnailstreamcache">IThumbnailStreamCache</a>
 

 

