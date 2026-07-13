---
UID: NF:wininet.CommitUrlCacheEntryW
title: CommitUrlCacheEntryW function (wininet.h)
description: Stores data in the specified file in the Internet cache and associates it with the specified URL. (Unicode)
helpviewer_keywords: ["CommitUrlCacheEntryW", "CommitUrlCacheEntryW function [WinINet]", "_inet_commiturlcacheentry_function", "wininet.commiturlcacheentry", "wininet.commiturlcacheentryw", "wininet/CommitUrlCacheEntryW"]
old-location: wininet\commiturlcacheentryw.htm
tech.root: wininet
ms.assetid: 0124e664-85a3-4637-9d91-7ec23025a87b
ms.date: 12/05/2018
ms.keywords: CommitUrlCacheEntryW, CommitUrlCacheEntryW function [WinINet], _inet_commiturlcacheentry_function, wininet.commiturlcacheentry, wininet.commiturlcacheentryw, wininet/CommitUrlCacheEntryW
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
 - CommitUrlCacheEntryW
 - wininet/CommitUrlCacheEntryW
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
 - CommitUrlCacheEntryW
---

# CommitUrlCacheEntryW function


## -description

Stores data in the specified file in the Internet cache and associates it with the specified URL.

## -parameters

### -param lpszUrlName [in]

Pointer to a string variable that contains the source name of the cache entry. The name string must be unique and should not contain any escape characters.

### -param lpszLocalFileName [in]

Pointer to a string variable that contains the name of the local file that is being cached. This should be the same name as that returned by 
<b>CreateUrlCacheEntryW</b>.

### -param ExpireTime [in]

<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the expire date and time (in Greenwich mean time) of the file that is being cached. If the expire date and time is unknown, set this parameter to zero.

### -param LastModifiedTime [in]

<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the last modified date and time (in Greenwich mean time) of the URL that is being cached. If the last modified date and time is unknown, set this parameter to zero.

### -param CacheEntryType [in]

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

### -param lpszHeaderInfo [in]

Pointer to the buffer that contains the header information. If this parameter is not <b>NULL</b>, the header information is treated as extended attributes of the URL that are returned in the 
<b>lpHeaderInfo</b> 
member of the <a href="/windows/desktop/api/wininet/ns-wininet-internet_cache_entry_infoa">INTERNET_CACHE_ENTRY_INFO</a> structure.

### -param cchHeaderInfo [in]

Size of the header information, in <b>TCHARs</b>. If 
<i>lpHeaderInfo</i> is not <b>NULL</b>, this value is assumed to indicate the size of the buffer that  stores the header information. An application can maintain headers as part of the data and provide 
<i>cchHeaderInfo</i> together with a <b>NULL</b> value for 
<i>lpHeaderInfo</i>.

### -param lpszFileExtension [in]

This parameter is reserved and must be <b>NULL</b>.

### -param lpszOriginalUrl [in]

Pointer to a string  that contains the original URL, if redirection has occurred.

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. The following are possible error values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DISK_FULL</b></dt>
</dl>
</td>
<td width="60%">
The cache storage is full.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified local file is not found.

</td>
</tr>
</table>

## -remarks

The STICKY_CACHE_ENTRY type is used to make cache entries exempt from scavenging. The default exempt time for entries set using 
<b>CommitUrlCacheEntryW</b> is ten minutes. The exempt time can be changed by setting the expires time parameter in the <a href="/windows/desktop/api/wininet/ns-wininet-internet_cache_entry_infoa">INTERNET_CACHE_ENTRY_INFO</a> structure in the call to the 
<a href="/windows/desktop/api/wininet/nf-wininet-seturlcacheentryinfoa">SetUrlCacheEntryInfo</a> function.

If the cache storage is full, 
<b>CommitUrlCacheEntryW</b> invokes cache cleanup to make space for this new file. If the cache entry already exists, the function overwrites the entry if it is not in use. An entry is in use when it has been retrieved with either 
<a href="/windows/desktop/api/wininet/nf-wininet-retrieveurlcacheentrystreama">RetrieveUrlCacheEntryStream</a> or 
<a href="/windows/desktop/api/wininet/nf-wininet-retrieveurlcacheentryfilea">RetrieveUrlCacheEntryFile</a>.

Clients that add entries to the cache should set the headers to at least "HTTP/1.0 200 OK\r\n\r\n"; otherwise, Microsoft Internet Explorer and other client applications should disregard the entry.

See <a href="/windows/desktop/WinInet/caching">Caching</a> for example code calling <b>CreateUrlCacheEntryW</b>.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines CommitUrlCacheEntry as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/caching">Caching</a>



<a href="/windows/desktop/WinInet/wininet-functions"> WinINet Functions</a>
