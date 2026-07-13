---
UID: NF:wininet.GetUrlCacheEntryInfoA
title: GetUrlCacheEntryInfoA function (wininet.h)
description: Retrieves information about a cache entry. (ANSI)
helpviewer_keywords: ["GetUrlCacheEntryInfoA", "wininet/GetUrlCacheEntryInfoA"]
old-location: wininet\geturlcacheentryinfo.htm
tech.root: wininet
ms.assetid: 0f70bcef-2d56-4765-a44e-4549b4ae2ced
ms.date: 12/05/2018
ms.keywords: GetUrlCacheEntryInfo, GetUrlCacheEntryInfo function [WinINet], GetUrlCacheEntryInfoA, GetUrlCacheEntryInfoW, _inet_geturlcacheentryinfo_function, wininet.geturlcacheentryinfo, wininet/GetUrlCacheEntryInfo, wininet/GetUrlCacheEntryInfoA, wininet/GetUrlCacheEntryInfoW
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetUrlCacheEntryInfoW (Unicode) and GetUrlCacheEntryInfoA (ANSI)
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
 - GetUrlCacheEntryInfoA
 - wininet/GetUrlCacheEntryInfoA
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
 - GetUrlCacheEntryInfo
 - GetUrlCacheEntryInfoA
 - GetUrlCacheEntryInfoW
---

# GetUrlCacheEntryInfoA function


## -description

Retrieves information about a cache entry.

## -parameters

### -param lpszUrlName [in]

A pointer to a null-terminated string that contains the name of the cache entry. The name string should not contain any escape characters.

### -param lpCacheEntryInfo [out]

A pointer to an 
<a href="/windows/desktop/api/wininet/ns-wininet-internet_cache_entry_infoa">INTERNET_CACHE_ENTRY_INFO</a> structure that receives information about the cache entry. A buffer should be allocated for this parameter. 

Since the required size of the buffer is not known in advance,  it is best to allocate a buffer adequate to handle the size of most <a href="/windows/desktop/api/wininet/ns-wininet-internet_cache_entry_infoa">INTERNET_CACHE_ENTRY_INFO</a> entries. There is no cache entry size limit, so applications that need to enumerate the cache must be prepared to allocate variable-sized buffers.

### -param lpcbCacheEntryInfo [in, out]

A pointer to a variable that specifies the size of the 
<i>lpCacheEntryInfo</i> buffer, in bytes. When the function returns, the variable contains the number of bytes copied to the buffer, or the required size of the buffer, in bytes.

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Possible error values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified cache entry is not found in the cache.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The size of 
<i>lpCacheEntryInfo</i> as specified by 
<i>lpdwCacheEntryInfoBufferSize</i> is not sufficient to contain all the information. The value returned in 
<i>lpdwCacheEntryInfoBufferSize</i> indicates the buffer size necessary to contain all the information.

</td>
</tr>
</table>

## -remarks

<b>GetUrlCacheEntryInfo</b> does not do any URL parsing, so a URL containing an anchor (#) will not be found in the cache, even if the resource is cached. For example, if the URL `http://example.com/example.htm#sample` is passed, the function returns <b>ERROR_FILE_NOT_FOUND</b> even if `http://example.com/example.htm` is in the cache.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines GetUrlCacheEntryInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/caching">Caching</a>



<a href="/windows/desktop/WinInet/wininet-functions"> WinINet Functions</a>
