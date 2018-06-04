---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _WTS_CACHE_STATS_UN structure


## -description


Contains cache statistics.


## -struct-fields




### -field ProtocolCache

A <a href="https://msdn.microsoft.com/94e699f4-278c-45fd-88e2-42f97e7ea305">WTS_PROTOCOL_CACHE</a> structure that contains information about the number of times that requested data is found in and read from the cache.


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



This union is a member of the <a href="https://msdn.microsoft.com/3c29596f-77c6-415b-bf97-529f70b9d9fe">WTS_CACHE_STATS</a> structure. The <b>Specific</b> member of that structure contains an integer index that specifies which  member of the <b>WTS_CACHE_STATS_UN</b> union contains the cache data.



