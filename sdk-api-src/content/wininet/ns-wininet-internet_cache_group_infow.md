---
UID: NS:wininet._INTERNET_CACHE_GROUP_INFOW
title: INTERNET_CACHE_GROUP_INFOW (wininet.h)
description: Contains the information for a particular cache group. (Unicode)
helpviewer_keywords: ["*LPINTERNET_CACHE_GROUP_INFOW","INTERNET_CACHE_GROUP_INFO","INTERNET_CACHE_GROUP_INFO structure [WinINet]","INTERNET_CACHE_GROUP_INFOA","INTERNET_CACHE_GROUP_INFOW","LPINTERNET_CACHE_GROUP_INFO","LPINTERNET_CACHE_GROUP_INFO structure pointer [WinINet]","_inet_internet_cache_group_info_structure","wininet.internet_cache_group_info","wininet/INTERNET_CACHE_GROUP_INFO","wininet/INTERNET_CACHE_GROUP_INFOA","wininet/INTERNET_CACHE_GROUP_INFOW","wininet/LPINTERNET_CACHE_GROUP_INFO"]
old-location: wininet\internet_cache_group_info.htm
tech.root: wininet
ms.assetid: d1c30fee-b8a3-472d-91a5-9d081f66b007
ms.date: 12/05/2018
ms.keywords: '*LPINTERNET_CACHE_GROUP_INFOW, INTERNET_CACHE_GROUP_INFO, INTERNET_CACHE_GROUP_INFO structure [WinINet], INTERNET_CACHE_GROUP_INFOA, INTERNET_CACHE_GROUP_INFOW, LPINTERNET_CACHE_GROUP_INFO, LPINTERNET_CACHE_GROUP_INFO structure pointer [WinINet], _inet_internet_cache_group_info_structure, wininet.internet_cache_group_info, wininet/INTERNET_CACHE_GROUP_INFO, wininet/INTERNET_CACHE_GROUP_INFOA, wininet/INTERNET_CACHE_GROUP_INFOW, wininet/LPINTERNET_CACHE_GROUP_INFO'
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
targetos: Windows
req.typenames: INTERNET_CACHE_GROUP_INFOW, *LPINTERNET_CACHE_GROUP_INFOW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _INTERNET_CACHE_GROUP_INFOW
 - wininet/_INTERNET_CACHE_GROUP_INFOW
 - LPINTERNET_CACHE_GROUP_INFOW
 - wininet/LPINTERNET_CACHE_GROUP_INFOW
 - INTERNET_CACHE_GROUP_INFOW
 - wininet/INTERNET_CACHE_GROUP_INFOW
dev_langs:
 - c++
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

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines INTERNET_CACHE_GROUP_INFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wininet/nf-wininet-geturlcachegroupattributea">GetUrlCacheGroupAttribute</a>



<a href="/windows/desktop/api/wininet/nf-wininet-seturlcachegroupattributea">SetUrlCacheGroupAttribute</a>
