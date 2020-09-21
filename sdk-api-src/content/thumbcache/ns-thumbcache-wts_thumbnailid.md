---
UID: NS:thumbcache.WTS_THUMBNAILID
title: WTS_THUMBNAILID (thumbcache.h)
description: Contains a unique identifier for a thumbnail in the system thumbnail cache.
helpviewer_keywords: ["WTS_THUMBNAILID","WTS_THUMBNAILID structure [Windows Shell]","_shell_WTS_THUMBNAILID","shell.WTS_THUMBNAILID","thumbcache/WTS_THUMBNAILID"]
old-location: shell\WTS_THUMBNAILID.htm
tech.root: shell
ms.assetid: 3006d1a8-c9cf-4528-9aea-8ad5d97ddff0
ms.date: 12/05/2018
ms.keywords: WTS_THUMBNAILID, WTS_THUMBNAILID structure [Windows Shell], _shell_WTS_THUMBNAILID, shell.WTS_THUMBNAILID, thumbcache/WTS_THUMBNAILID
req.header: thumbcache.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Thumbcache.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WTS_THUMBNAILID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WTS_THUMBNAILID
 - thumbcache/WTS_THUMBNAILID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Thumbcache.h
api_name:
 - WTS_THUMBNAILID
---

# WTS_THUMBNAILID structure


## -description

Contains a unique identifier for a thumbnail in the system thumbnail cache.

## -struct-fields

### -field rgbKey

Type: <b>BYTE[16]</b>

An array of 16 bytes that make up a unique identifier for a thumbnail in the system thumbnail cache.

## -remarks

A <b>WTS_THUMBNAILID</b> may be retrieved from <a href="/windows/desktop/api/thumbcache/nf-thumbcache-ithumbnailcache-getthumbnail">IThumbnailCache::GetThumbnail</a> when a new thumbnail is cached. To access the cached thumbnail by its ID, the <b>WTS_THUMBNAILID</b> may then be passed to <a href="/windows/desktop/api/thumbcache/nf-thumbcache-ithumbnailcache-getthumbnailbyid">IThumbnailCache::GetThumbnailByID</a>.

## -see-also

<a href="/windows/desktop/api/thumbcache/nf-thumbcache-ithumbnailcache-getthumbnail">IThumbnailCache::GetThumbnail</a>



<a href="/windows/desktop/api/thumbcache/nf-thumbcache-ithumbnailcache-getthumbnailbyid">IThumbnailCache::GetThumbnailByID</a>