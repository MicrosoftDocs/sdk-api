---
UID: NS:winineti._INTERNET_CACHE_CONFIG_INFOA
title: "_INTERNET_CACHE_CONFIG_INFOA"
author: windows-sdk-content
description: Contains information about the configuration of the Internet cache.
old-location: wininet\internet_cache_config_info.htm
tech.root: WinInet
ms.assetid: 39019a94-6f14-4758-86f7-aba598e23d2e
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*LPINTERNET_CACHE_CONFIG_INFOA, INTERNET_CACHE_CONFIG_INFO, INTERNET_CACHE_CONFIG_INFO structure [WinINet], INTERNET_CACHE_CONFIG_INFOA, PINTERNET_CACHE_CONFIG_INFO, PINTERNET_CACHE_CONFIG_INFO structure pointer [WinINet], _INTERNET_CACHE_CONFIG_INFOA, wininet.internet_cache_config_info, winineti/INTERNET_CACHE_CONFIG_INFO, winineti/PINTERNET_CACHE_CONFIG_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winineti.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP4 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP4 [desktop apps only]
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
 - Winineti.h
api_name:
 - INTERNET_CACHE_CONFIG_INFO
product: Windows
targetos: Windows
req.typenames: INTERNET_CACHE_CONFIG_INFOA, *LPINTERNET_CACHE_CONFIG_INFOA
req.redist: 
---

# _INTERNET_CACHE_CONFIG_INFOA structure


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
 

 

