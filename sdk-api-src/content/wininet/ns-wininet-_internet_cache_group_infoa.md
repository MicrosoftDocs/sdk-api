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

# _INTERNET_CACHE_GROUP_INFOA structure


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
 

 

