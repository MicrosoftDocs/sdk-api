---
UID: NS:wininet._INTERNET_CACHE_GROUP_INFOW
title: INTERNET_CACHE_GROUP_INFOW
author: windows-sdk-content
description: Contains the information for a particular cache group.
old-location: wininet\internet_cache_group_info.htm
tech.root: wininet
ms.assetid: d1c30fee-b8a3-472d-91a5-9d081f66b007
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPINTERNET_CACHE_GROUP_INFOW, INTERNET_CACHE_GROUP_INFO, INTERNET_CACHE_GROUP_INFO structure [WinINet], INTERNET_CACHE_GROUP_INFOA, INTERNET_CACHE_GROUP_INFOW, LPINTERNET_CACHE_GROUP_INFO, LPINTERNET_CACHE_GROUP_INFO structure pointer [WinINet], _inet_internet_cache_group_info_structure, wininet.internet_cache_group_info, wininet/INTERNET_CACHE_GROUP_INFO, wininet/INTERNET_CACHE_GROUP_INFOA, wininet/INTERNET_CACHE_GROUP_INFOW, wininet/LPINTERNET_CACHE_GROUP_INFO"
ms.topic: struct
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: INTERNET_CACHE_GROUP_INFOW (Unicode) and INTERNET_CACHE_GROUP_INFOA (ANSI)
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
 - Wininet.h
api_name:
 - INTERNET_CACHE_GROUP_INFO
 - INTERNET_CACHE_GROUP_INFOA
 - INTERNET_CACHE_GROUP_INFOW
product: Windows
targetos: Windows
req.typenames: INTERNET_CACHE_GROUP_INFOW, *LPINTERNET_CACHE_GROUP_INFOW
req.redist: 
---

# INTERNET_CACHE_GROUP_INFOW structure


## -description


Contains the information for a particular cache group. 


## -struct-fields




### -field dwGroupSize

Size of the structure, <b>TCHARs</b>. 


### -field dwGroupFlags

Group flags. Currently, the only value defined is CACHEGROUP_FLAG_NONPURGEABLE, which indicates that the cache entries in this group will not be removed by the cache manager. 


### -field dwGroupType

Group type. Currently, the only value defined is CACHEGROUP_TYPE_INVALID. 


### -field dwDiskUsage

Current disk usage of this cache group, in kilobytes. 


### -field dwDiskQuota

Disk quota for this cache group, in kilobytes. 


### -field dwOwnerStorage

Array  that can be used by a client application to store information related to the group. 


### -field szGroupName

Group name. 


## -remarks



<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/5e4e5666-1999-4bea-9b3e-f435f5dcfff8">GetUrlCacheGroupAttribute</a>



<a href="https://msdn.microsoft.com/dd4e94cd-0fe5-414a-8a43-8777403e8a45">SetUrlCacheGroupAttribute</a>
 

 

