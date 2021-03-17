---
UID: NF:wininet.FindCloseUrlCache
title: FindCloseUrlCache function (wininet.h)
description: Closes the specified cache enumeration handle.
helpviewer_keywords: ["FindCloseUrlCache","FindCloseUrlCache function [WinINet]","_inet_findcloseurlcache_function","wininet.findcloseurlcache","wininet/FindCloseUrlCache"]
old-location: wininet\findcloseurlcache.htm
tech.root: wininet
ms.assetid: 54fc7bea-4cc1-4034-93c3-49ec88817648
ms.date: 12/05/2018
ms.keywords: FindCloseUrlCache, FindCloseUrlCache function [WinINet], _inet_findcloseurlcache_function, wininet.findcloseurlcache, wininet/FindCloseUrlCache
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
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FindCloseUrlCache
 - wininet/FindCloseUrlCache
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wininet.dll
api_name:
 - FindCloseUrlCache
---

# FindCloseUrlCache function


## -description

Closes the specified cache enumeration handle.

## -parameters

### -param hEnumHandle [in]

Handle returned by a previous call to the 
<a href="/windows/desktop/api/wininet/nf-wininet-findfirsturlcacheentrya">FindFirstUrlCacheEntry</a> function.

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/WinInet/caching">Caching</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>