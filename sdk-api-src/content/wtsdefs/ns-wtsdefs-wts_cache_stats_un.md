---
UID: NS:wtsdefs._WTS_CACHE_STATS_UN
title: WTS_CACHE_STATS_UN (wtsdefs.h)
author: windows-sdk-content
description: Contains cache statistics.
old-location: termserv\wts_cache_stats_un.htm
tech.root: TermServ
ms.assetid: e6abb47e-248b-482d-9206-936092c391ce
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: '*PWTS_CACHE_STATS_UN, PWRDS_CACHE_STATS_UN, PWRDS_CACHE_STATS_UN union pointer [Remote Desktop Services], PWTS_CACHE_STATS_UN, PWTS_CACHE_STATS_UN union pointer [Remote Desktop Services], WRDS_CACHE_STATS_UN, WRDS_CACHE_STATS_UN union [Remote Desktop Services], WTS_CACHE_STATS_UN, WTS_CACHE_STATS_UN union [Remote Desktop Services], termserv.wts_cache_stats_un, wtsdefs/PWRDS_CACHE_STATS_UN, wtsdefs/PWTS_CACHE_STATS_UN, wtsdefs/WRDS_CACHE_STATS_UN, wtsdefs/WTS_CACHE_STATS_UN'
ms.topic: struct
f1_keywords:
- wtsdefs/WTS_CACHE_STATS_UN
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
- WTS_CACHE_STATS_UN
product: Windows
targetos: Windows
req.typenames: WTS_CACHE_STATS_UN, *PWTS_CACHE_STATS_UN
req.redist: 
ms.custom: 19H1
---

# WTS_CACHE_STATS_UN structure


## -description


Contains cache statistics.


## -struct-fields




### -field ProtocolCache

A <a href="https://docs.microsoft.com/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_protocol_cache">WTS_PROTOCOL_CACHE</a> structure that contains information about the number of times that requested data is found in and read from the cache.


### -field ProtocolCache.case

 


### -field ProtocolCache.case.1

 


### -field TShareCacheStats

Share cache statistics.


### -field TShareCacheStats.case

 


### -field TShareCacheStats.case.2

 


### -field Reserved

Reserved protocol specific data. The maximum size, in bytes, of this data is WTS_MAX_CACHE_RESERVED multiplied by the length of an unsigned long integer.


### -field Reserved.case

 


### -field Reserved.case.3

 


### -field switch_type

 


### -field switch_type.DWORD

 




## -remarks



This union is a member of the <a href="https://docs.microsoft.com/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_cache_stats">WTS_CACHE_STATS</a> structure. The <b>Specific</b> member of that structure contains an integer index that specifies which  member of the <b>WTS_CACHE_STATS_UN</b> union contains the cache data.



