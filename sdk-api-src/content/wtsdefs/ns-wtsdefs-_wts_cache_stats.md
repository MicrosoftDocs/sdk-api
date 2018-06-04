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

# _WTS_CACHE_STATS structure


## -description


Contains protocol cache statistics.


## -struct-fields




### -field Specific

An integer index that specifies the <a href="https://msdn.microsoft.com/e6abb47e-248b-482d-9206-936092c391ce">WTS_CACHE_STATS_UN</a> union member that contains the cache data. This can be one of the following values.



#### 1

The cache data is contained in the <b>ProtocolCache</b> member.



#### 2

The cache data is contained in the <b>TShareCacheStats</b> member.



#### 3

The cache data is contained in the <b>Reserved</b> member.


### -field Data

A <a href="https://msdn.microsoft.com/e6abb47e-248b-482d-9206-936092c391ce">WTS_CACHE_STATS_UN</a> union that contains the cache statistics.


### -field Data.switch_is

 


### -field Data.switch_is.Specific

 


### -field ProtocolType

An integer that specifies the protocol type. This is not currently used by the Remote Desktop Services service.


### -field Length

An integer that contains the length of the data in the <b>Reserved</b> member of the <a href="https://msdn.microsoft.com/e6abb47e-248b-482d-9206-936092c391ce">WTS_CACHE_STATS_UN</a> union. The maximum size is WTS_MAX_CACHE_RESERVED multiplied by the length of an unsigned long integer.


## -remarks



This structure is a member of the <a href="https://msdn.microsoft.com/20e66033-fc79-49c9-af0e-abaf6e4ba501">WTS_PROTOCOL_STATUS</a> structure.



