---
UID: NE:thumbnailstreamcache.ThumbnailStreamCacheOptions
title: ThumbnailStreamCacheOptions
author: windows-sdk-content
description: Defines the cache options used by the IThumbnailStreamCache interface.
old-location: shell\thumbnailstreamcacheoptions.htm
old-project: shell
ms.assetid: E148138E-E41F-4274-B40A-7BF49BCF2AB4
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: AllowSmallerSize, ExtractIfNotCached, ResizeThumbnail, ReturnOnlyIfCached, ThumbnailStreamCacheOptions, ThumbnailStreamCacheOptions enumeration [Windows Shell], shell.thumbnailstreamcacheoptions, thumbnailstreamcache/AllowSmallerSize, thumbnailstreamcache/ExtractIfNotCached, thumbnailstreamcache/ResizeThumbnail, thumbnailstreamcache/ReturnOnlyIfCached, thumbnailstreamcache/ThumbnailStreamCacheOptions
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: thumbnailstreamcache.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Thumbcache.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: ThumbnailStreamCacheOptions
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - thumbnailstreamcache.h
api_name:
 - ThumbnailStreamCacheOptions
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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
 

 

