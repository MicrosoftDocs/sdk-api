---
UID: NS:thumbcache.WTS_THUMBNAILID
title: WTS_THUMBNAILID
author: windows-sdk-content
description: Contains a unique identifier for a thumbnail in the system thumbnail cache.
old-location: shell\WTS_THUMBNAILID.htm
old-project: shell
ms.assetid: 3006d1a8-c9cf-4528-9aea-8ad5d97ddff0
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: WTS_THUMBNAILID, WTS_THUMBNAILID structure [Windows Shell], _shell_WTS_THUMBNAILID, shell.WTS_THUMBNAILID, thumbcache/WTS_THUMBNAILID
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: WTS_THUMBNAILID
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Thumbcache.h
api_name:
 - WTS_THUMBNAILID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# WTS_THUMBNAILID structure


## -description


Contains a unique identifier for a thumbnail in the system thumbnail cache.


## -struct-fields




### -field rgbKey

Type: <b>BYTE[16]</b>

An array of 16 bytes that make up a unique identifier for a thumbnail in the system thumbnail cache.  				
				


## -remarks



A <b>WTS_THUMBNAILID</b> may be retrieved from <a href="https://msdn.microsoft.com/0fcfe68b-5d36-4be1-a468-b5c2d7af0651">IThumbnailCache::GetThumbnail</a> when a new thumbnail is cached. To access the cached thumbnail by its ID, the <b>WTS_THUMBNAILID</b> may then be passed to <a href="https://msdn.microsoft.com/3b5069e2-f20b-4c43-a9e7-334366980f5c">IThumbnailCache::GetThumbnailByID</a>.




## -see-also




<a href="https://msdn.microsoft.com/0fcfe68b-5d36-4be1-a468-b5c2d7af0651">IThumbnailCache::GetThumbnail</a>



<a href="https://msdn.microsoft.com/3b5069e2-f20b-4c43-a9e7-334366980f5c">IThumbnailCache::GetThumbnailByID</a>
 

 

