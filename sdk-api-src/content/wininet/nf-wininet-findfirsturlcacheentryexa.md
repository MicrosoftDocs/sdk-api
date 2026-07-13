---
UID: NF:wininet.FindFirstUrlCacheEntryExA
title: FindFirstUrlCacheEntryExA function (wininet.h)
description: Starts a filtered enumeration of the Internet cache. (ANSI)
helpviewer_keywords: ["FindFirstUrlCacheEntryExA", "wininet/FindFirstUrlCacheEntryExA"]
old-location: wininet\findfirsturlcacheentryex.htm
tech.root: wininet
ms.assetid: af17c809-2a9e-443a-b64a-93c028e3b71b
ms.date: 12/05/2018
ms.keywords: FindFirstUrlCacheEntryEx, FindFirstUrlCacheEntryEx function [WinINet], FindFirstUrlCacheEntryExA, FindFirstUrlCacheEntryExW, _inet_findfirsturlcacheentryex_function, wininet.findfirsturlcacheentryex, wininet/FindFirstUrlCacheEntryEx, wininet/FindFirstUrlCacheEntryExA, wininet/FindFirstUrlCacheEntryExW
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FindFirstUrlCacheEntryExW (Unicode) and FindFirstUrlCacheEntryExA (ANSI)
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
 - FindFirstUrlCacheEntryExA
 - wininet/FindFirstUrlCacheEntryExA
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
 - FindFirstUrlCacheEntryEx
 - FindFirstUrlCacheEntryExA
 - FindFirstUrlCacheEntryExW
---

# FindFirstUrlCacheEntryExA function


## -description

Starts a filtered enumeration of the Internet cache.

## -parameters

### -param lpszUrlSearchPattern [in]

A pointer to a string that contains the source name pattern to search for. This parameter can only be set to "cookie:", "visited:", or NULL. Set this parameter to "cookie:" to enumerate the cookies or "visited:" to enumerate the URL History entries in the cache. If this parameter is NULL, <b>FindFirstUrlCacheEntryEx</b> returns all content entries in the cache.

### -param dwFlags [in]

Controls the enumeration. No flags are currently implemented; this parameter must be set to zero.

### -param dwFilter [in]

A bitmask indicating the type of cache entry and its properties. The cache entry types include: history entries (URLHISTORY_CACHE_ENTRY),  cookie entries  (COOKIE_CACHE_ENTRY), and normal cached content (NORMAL_CACHE_ENTRY).

This parameter can be zero or more of the following property flags, and  cache type flags listed below.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>COOKIE_CACHE_ENTRY</dt>
</dl>
</td>
<td width="60%">
Cookie cache entry.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>EDITED_CACHE_ENTRY</dt>
</dl>
</td>
<td width="60%">
Cache entry file that has been edited externally. This cache entry type is exempt from scavenging. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>NORMAL_CACHE_ENTRY</dt>
</dl>
</td>
<td width="60%">
Normal cache entry; can be deleted to recover space for new entries.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>SPARSE_CACHE_ENTRY</dt>
</dl>
</td>
<td width="60%">
Partial response cache entry.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>STICKY_CACHE_ENTRY</dt>
</dl>
</td>
<td width="60%">
Sticky cache entry; exempt from scavenging.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>TRACK_OFFLINE_CACHE_ENTRY</dt>
</dl>
</td>
<td width="60%">
Not currently implemented.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>TRACK_ONLINE_CACHE_ENTRY</dt>
</dl>
</td>
<td width="60%">
Not currently implemented.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>URLHISTORY_CACHE_ENTRY</dt>
</dl>
</td>
<td width="60%">
Visited link cache entry.

</td>
</tr>
</table>

### -param GroupId [in]

ID of the cache group to be enumerated. Set this parameter to zero to enumerate all entries that are not grouped.

### -param lpFirstCacheEntryInfo [out]

Pointer to a 
<a href="/windows/desktop/api/wininet/ns-wininet-internet_cache_entry_infoa">INTERNET_CACHE_ENTRY_INFO</a> structure to receive the cache entry information.

### -param lpcbCacheEntryInfo [in, out]

Pointer to variable that indicates the size of 
the structure referenced by the <i>lpFirstCacheEntryInfo</i> parameter, in bytes.

### -param lpGroupAttributes [out]

This parameter is reserved and must be NULL.

### -param lpcbGroupAttributes [in, out]

This parameter is reserved and must be NULL.

### -param lpReserved [in]

This parameter is reserved and must be NULL.

## -returns

Returns a valid handle if successful, or NULL otherwise. To get specific error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. If the function finds no matching files, 
<b>GetLastError</b> returns ERROR_NO_MORE_FILES.

## -remarks

The handle returned from <b>FindFirstUrlCacheEntryEx</b> is used in all subsequent calls to <a href="/windows/desktop/api/wininet/nf-wininet-findnexturlcacheentryexa">FindNextUrlCacheEntryEx</a>. At the end of the enumeration, the application should call 
<a href="/windows/desktop/api/wininet/nf-wininet-findcloseurlcache">FindCloseUrlCache</a>.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines FindFirstUrlCacheEntryEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/caching">Caching</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
