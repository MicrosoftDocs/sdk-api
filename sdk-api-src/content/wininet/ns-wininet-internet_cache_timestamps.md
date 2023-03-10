---
UID: NS:wininet._INTERNET_CACHE_TIMESTAMPS
title: INTERNET_CACHE_TIMESTAMPS (wininet.h)
description: Contains the LastModified and Expire times for a resource stored in the Internet cache.
helpviewer_keywords: ["*LPINTERNET_CACHE_TIMESTAMPS","INTERNET_CACHE_TIMESTAMPS","INTERNET_CACHE_TIMESTAMPS structure [WinINet]","LPINTERNET_CACHE_TIMESTAMPS","LPINTERNET_CACHE_TIMESTAMPS structure pointer [WinINet]","_inet_internet_cache_timestamps_structure","wininet.internet_cache_timestamps","wininet/INTERNET_CACHE_TIMESTAMPS","wininet/LPINTERNET_CACHE_TIMESTAMPS"]
old-location: wininet\internet_cache_timestamps.htm
tech.root: wininet
ms.assetid: e0fc2d73-95b9-4466-8a80-ca3211fc58e1
ms.date: 12/05/2018
ms.keywords: '*LPINTERNET_CACHE_TIMESTAMPS, INTERNET_CACHE_TIMESTAMPS, INTERNET_CACHE_TIMESTAMPS structure [WinINet], LPINTERNET_CACHE_TIMESTAMPS, LPINTERNET_CACHE_TIMESTAMPS structure pointer [WinINet], _inet_internet_cache_timestamps_structure, wininet.internet_cache_timestamps, wininet/INTERNET_CACHE_TIMESTAMPS, wininet/LPINTERNET_CACHE_TIMESTAMPS'
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
targetos: Windows
req.typenames: INTERNET_CACHE_TIMESTAMPS, *LPINTERNET_CACHE_TIMESTAMPS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _INTERNET_CACHE_TIMESTAMPS
 - wininet/_INTERNET_CACHE_TIMESTAMPS
 - LPINTERNET_CACHE_TIMESTAMPS
 - wininet/LPINTERNET_CACHE_TIMESTAMPS
 - INTERNET_CACHE_TIMESTAMPS
 - wininet/INTERNET_CACHE_TIMESTAMPS
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
 - INTERNET_CACHE_TIMESTAMPS
---

# INTERNET_CACHE_TIMESTAMPS structure


## -description

Contains the LastModified and Expire times for a resource stored in the Internet cache.

## -struct-fields

### -field ftExpires

<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the Expires time.

### -field ftLastModified

<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the LastModified time.

## -remarks

This structure is returned in the buffer when calling 
<a href="/windows/desktop/api/wininet/nf-wininet-internetqueryoptiona">InternetQueryOption</a> with the 
<a href="/windows/desktop/WinInet/option-flags">INTERNET_OPTION_CACHE_TIMESTAMPS</a> flag.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wininet/nf-wininet-internetqueryoptiona">InternetQueryOption</a>