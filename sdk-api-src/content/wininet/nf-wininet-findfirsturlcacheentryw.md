---
UID: NF:wininet.FindFirstUrlCacheEntryW
title: FindFirstUrlCacheEntryW function (wininet.h)
description: Begins the enumeration of the Internet cache. (Unicode)
helpviewer_keywords: ["FindFirstUrlCacheEntry", "FindFirstUrlCacheEntry function [WinINet]", "FindFirstUrlCacheEntryW", "_inet_findfirsturlcacheentry_function", "wininet.findfirsturlcacheentry", "wininet/FindFirstUrlCacheEntry", "wininet/FindFirstUrlCacheEntryW"]
old-location: wininet\findfirsturlcacheentry.htm
tech.root: wininet
ms.assetid: e8407284-846b-4080-b75b-4805330e0f95
ms.date: 12/05/2018
ms.keywords: FindFirstUrlCacheEntry, FindFirstUrlCacheEntry function [WinINet], FindFirstUrlCacheEntryA, FindFirstUrlCacheEntryW, _inet_findfirsturlcacheentry_function, wininet.findfirsturlcacheentry, wininet/FindFirstUrlCacheEntry, wininet/FindFirstUrlCacheEntryA, wininet/FindFirstUrlCacheEntryW
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FindFirstUrlCacheEntryW (Unicode) and FindFirstUrlCacheEntryA (ANSI)
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
 - FindFirstUrlCacheEntryW
 - wininet/FindFirstUrlCacheEntryW
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
 - FindFirstUrlCacheEntry
 - FindFirstUrlCacheEntryA
 - FindFirstUrlCacheEntryW
---

# FindFirstUrlCacheEntryW function


## -description

Begins the enumeration of the Internet cache.

## -parameters

### -param lpszUrlSearchPattern [in]

A pointer to a string that contains the source name pattern to search for. This parameter can only be set to "cookie:", "visited:", or <b>NULL</b>. Set this parameter to "cookie:" to enumerate the cookies or "visited:" to enumerate the URL History entries in the cache. If this parameter is <b>NULL</b>, <b>FindFirstUrlCacheEntry</b> returns all content entries in the cache.

### -param lpFirstCacheEntryInfo [out]

Pointer to an 
<a href="/windows/desktop/api/wininet/ns-wininet-internet_cache_entry_infoa">INTERNET_CACHE_ENTRY_INFO</a> structure.

### -param lpcbCacheEntryInfo [in, out]

Pointer to a variable that specifies the size of the 
<i>lpFirstCacheEntryInfo</i> buffer, in bytes. When the function returns, the variable contains the number of bytes copied to the buffer, or the required size needed to retrieve the cache entry, in bytes.

## -returns

Returns a handle that the application can use in the 
<a href="/windows/desktop/api/wininet/nf-wininet-findnexturlcacheentrya">FindNextUrlCacheEntry</a> function to retrieve subsequent entries in the cache. If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

ERROR_INSUFFICIENT_BUFFER indicates that the size of 
<i>lpFirstCacheEntryInfo</i> as specified by 
<i>lpdwFirstCacheEntryInfoBufferSize</i> is not sufficient to contain all the information. The value returned in 
<i>lpdwFirstCacheEntryInfoBufferSize</i> indicates the buffer size necessary to contain all the information.

## -remarks

The handle returned from <b>FindFirstUrlCacheEntry</b> is used in all subsequent calls to <a href="/windows/desktop/api/wininet/nf-wininet-findnexturlcacheentrya">FindNextUrlCacheEntry</a>. At the end of the enumeration, the application should call 
<a href="/windows/desktop/api/wininet/nf-wininet-findcloseurlcache">FindCloseUrlCache</a>.

<b>FindFirstUrlCacheEntry</b> and 
<a href="/windows/desktop/api/wininet/nf-wininet-findnexturlcacheentrya">FindNextUrlCacheEntry</a> return variable size information. If ERROR_INSUFFICIENT_BUFFER is returned, the application should allocate a buffer of the size specified by 
<i>lpdwFirstCacheEntryInfoBufferSize</i>. For more information, see 
<a href="/windows/desktop/WinInet/appendix-b-using-buffers">Using Buffers</a>.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines FindFirstUrlCacheEntry as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/caching">Caching</a>



<a href="/windows/desktop/WinInet/wininet-functions"> WinINet Functions</a>
