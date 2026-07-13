---
UID: NF:wininet.RetrieveUrlCacheEntryStreamA
title: RetrieveUrlCacheEntryStreamA function (wininet.h)
description: Provides the most efficient and implementation-independent way to access the cache data. (ANSI)
helpviewer_keywords: ["RetrieveUrlCacheEntryStreamA", "wininet/RetrieveUrlCacheEntryStreamA"]
old-location: wininet\retrieveurlcacheentrystream.htm
tech.root: wininet
ms.assetid: 0414efb0-d91b-46f0-9fee-0b69ef823029
ms.date: 12/05/2018
ms.keywords: RetrieveUrlCacheEntryStream, RetrieveUrlCacheEntryStream function [WinINet], RetrieveUrlCacheEntryStreamA, RetrieveUrlCacheEntryStreamW, _inet_retrieveurlcacheentrystream_function, wininet.retrieveurlcacheentrystream, wininet/RetrieveUrlCacheEntryStream, wininet/RetrieveUrlCacheEntryStreamA, wininet/RetrieveUrlCacheEntryStreamW
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RetrieveUrlCacheEntryStreamW (Unicode) and RetrieveUrlCacheEntryStreamA (ANSI)
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
 - RetrieveUrlCacheEntryStreamA
 - wininet/RetrieveUrlCacheEntryStreamA
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
 - RetrieveUrlCacheEntryStream
 - RetrieveUrlCacheEntryStreamA
 - RetrieveUrlCacheEntryStreamW
---

# RetrieveUrlCacheEntryStreamA function


## -description

Provides the most efficient and implementation-independent way to access the cache data.

## -parameters

### -param lpszUrlName [in]

Pointer to a null-terminated string that contains the source name of the cache entry. This must be a unique name. The name string should not contain any escape characters.

### -param lpCacheEntryInfo [out]

Pointer to an 
<a href="/windows/desktop/api/wininet/ns-wininet-internet_cache_entry_infoa">INTERNET_CACHE_ENTRY_INFO</a> structure that receives information about the cache entry.

### -param lpcbCacheEntryInfo [in, out]

Pointer to a variable that specifies the size, in bytes, of the 
<i>lpCacheEntryInfo</i> buffer. When the function returns, the variable receives the number of bytes copied to the buffer or the required size, in bytes, of the buffer. Note that this buffer size must accommodate both the <a href="/windows/desktop/api/wininet/ns-wininet-internet_cache_entry_infoa">INTERNET_CACHE_ENTRY_INFO</a> structure and the associated strings that are stored immediately following it.

### -param fRandomRead [in]

Whether the stream is open for random access. Set the flag to <b>TRUE</b> to open the stream for random access.

### -param dwReserved [in]

This parameter is reserved and must be 0.

## -returns

If the function succeeds, the function returns a valid handle for use in the 
<a href="/windows/desktop/api/wininet/nf-wininet-readurlcacheentrystream">ReadUrlCacheEntryStream</a> and 
<a href="/windows/desktop/api/wininet/nf-wininet-unlockurlcacheentrystream">UnlockUrlCacheEntryStream</a> functions.

If the function fails, it returns <b>NULL</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

Possible error values include the following.

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
The cache entry specified by the source name is not found in the cache storage.

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

<b>RetrieveUrlCacheEntryStream</b> does not do any URL parsing, so a URL containing an anchor (#) will not be found in the cache, even if the resource is cached. For example, if the URL http://adatum.com/example.htm#sample is passed, the function returns ERROR_FILE_NOT_FOUND even if http://adatum.com/example.htm is in the cache.

Cache clients that do not need URL data in the form of a file should use this function to access the data for a particular URL.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines RetrieveUrlCacheEntryStream as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/caching">Caching</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
