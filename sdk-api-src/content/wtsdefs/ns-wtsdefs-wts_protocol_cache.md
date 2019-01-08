---
UID: NS:wtsdefs._WTS_PROTOCOL_CACHE
title: WTS_PROTOCOL_CACHE
author: windows-sdk-content
description: Contains the number of cache reads and cache hits.
old-location: termserv\wts_protocol_cache.htm
tech.root: termserv
ms.assetid: 94e699f4-278c-45fd-88e2-42f97e7ea305
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PWTS_PROTOCOL_CACHE, PWRDS_PROTOCOL_CACHE, PWRDS_PROTOCOL_CACHE structure pointer [Remote Desktop Services], PWTS_PROTOCOL_CACHE, PWTS_PROTOCOL_CACHE structure pointer [Remote Desktop Services], WRDS_PROTOCOL_CACHE, WRDS_PROTOCOL_CACHE structure [Remote Desktop Services], WTS_PROTOCOL_CACHE, WTS_PROTOCOL_CACHE structure [Remote Desktop Services], termserv.wts_protocol_cache, wtsdefs/PWRDS_PROTOCOL_CACHE, wtsdefs/PWTS_PROTOCOL_CACHE, wtsdefs/WRDS_PROTOCOL_CACHE, wtsdefs/WTS_PROTOCOL_CACHE"
ms.topic: struct
req.header: wtsdefs.h
req.include-header: Wtsprotocol.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
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
 - Wtsdefs.h
api_name:
 - WTS_PROTOCOL_CACHE
product: Windows
targetos: Windows
req.typenames: WTS_PROTOCOL_CACHE, *PWTS_PROTOCOL_CACHE
req.redist: 
---

# WTS_PROTOCOL_CACHE structure


## -description


Contains the number of cache reads and cache hits.


## -struct-fields




### -field CacheReads

An integer that contains the number of times cached data was read.


### -field CacheHits

An integer that contains the number of times the cache was hit. A cache hit occurs if required data is found in the cache rather than in main memory or on disk. If the data is found in the cache, it is read from the cache.

