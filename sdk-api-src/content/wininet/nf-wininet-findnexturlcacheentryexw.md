---
UID: NF:wininet.FindNextUrlCacheEntryExW
title: FindNextUrlCacheEntryExW function (wininet.h)
description: Finds the next cache entry in a cache enumeration started by the FindFirstUrlCacheEntryEx function. (Unicode)
helpviewer_keywords: ["FindNextUrlCacheEntryEx", "FindNextUrlCacheEntryEx function [WinINet]", "FindNextUrlCacheEntryExW", "_inet_findnexturlcacheentryex_function", "wininet.findnexturlcacheentryex", "wininet/FindNextUrlCacheEntryEx", "wininet/FindNextUrlCacheEntryExW"]
old-location: wininet\findnexturlcacheentryex.htm
tech.root: wininet
ms.assetid: 39484e35-cd25-4e48-ace0-16033d3e6954
ms.date: 12/05/2018
ms.keywords: FindNextUrlCacheEntryEx, FindNextUrlCacheEntryEx function [WinINet], FindNextUrlCacheEntryExA, FindNextUrlCacheEntryExW, _inet_findnexturlcacheentryex_function, wininet.findnexturlcacheentryex, wininet/FindNextUrlCacheEntryEx, wininet/FindNextUrlCacheEntryExA, wininet/FindNextUrlCacheEntryExW
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FindNextUrlCacheEntryExW (Unicode) and FindNextUrlCacheEntryExA (ANSI)
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
 - FindNextUrlCacheEntryExW
 - wininet/FindNextUrlCacheEntryExW
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
 - FindNextUrlCacheEntryEx
 - FindNextUrlCacheEntryExA
 - FindNextUrlCacheEntryExW
---

# FindNextUrlCacheEntryExW function


## -description

Finds the next cache entry in a cache enumeration started by the 
<a href="/windows/desktop/api/wininet/nf-wininet-findfirsturlcacheentryexa">FindFirstUrlCacheEntryEx</a> function.

## -parameters

### -param hEnumHandle [in]

Handle returned by 
<a href="/windows/desktop/api/wininet/nf-wininet-findfirsturlcacheentryexa">FindFirstUrlCacheEntryEx</a>, which started a cache enumeration.

### -param lpNextCacheEntryInfo [in, out]

Pointer to the  
<a href="/windows/desktop/api/wininet/ns-wininet-internet_cache_entry_infoa">INTERNET_CACHE_ENTRY_INFO</a> structure that receives the cache entry information.

### -param lpcbCacheEntryInfo [in, out]

Pointer to a variable that indicates the size of the buffer, in bytes.

### -param lpGroupAttributes

This parameter is reserved and must be <b>NULL</b>.

### -param lpcbGroupAttributes

This parameter is reserved and must be <b>NULL</b>.

### -param lpReserved

This parameter is reserved.

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get specific error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Continue to call <b>FindNextUrlCacheEntryEx</b> until the last item in the cache is returned.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines FindNextUrlCacheEntryEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/caching">Caching</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
