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

# _INTERNET_CACHE_CONFIG_INFOW structure


## -description


Contains information about the configuration of the Internet cache.


## -struct-fields




### -field dwStructSize

Size of this structure, in bytes. This value can be used to help determine the version of the cache system.


### -field dwContainer

The container that the rest of the data in the struct applies to. 0 (zero) indicates the content container.


### -field dwQuota

The cache quota limit of the container specified in kilobytes.


### -field dwReserved4

Reserved.


### -field fPerUser

Reserved.


### -field dwSyncMode

Reserved.


### -field dwNumCachePaths

Reserved.


### -field CachePath

The cache path for the container in <b>dwContainer</b>.


### -field dwCacheSize

Reserved.


### -field CachePaths

Reserved.


### -field dwNormalUsage

The cache size of the container specified in kilobytes.


### -field dwExemptUsage

The number of kilobytes for this container exempt from scavenging.


## -remarks



<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/93a29a4f-57bf-497c-a7b1-3960935590f9">GetUrlCacheConfigInfo</a>
 

 

