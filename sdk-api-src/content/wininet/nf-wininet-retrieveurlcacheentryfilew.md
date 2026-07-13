---
UID: NF:wininet.RetrieveUrlCacheEntryFileW
title: RetrieveUrlCacheEntryFileW function (wininet.h)
description: Locks the cache entry file associated with the specified URL. (Unicode)
helpviewer_keywords: ["RetrieveUrlCacheEntryFile", "RetrieveUrlCacheEntryFile function [WinINet]", "RetrieveUrlCacheEntryFileW", "_inet_retrieveurlcacheentryfile_function", "wininet.retrieveurlcacheentryfile", "wininet/RetrieveUrlCacheEntryFile", "wininet/RetrieveUrlCacheEntryFileW"]
old-location: wininet\retrieveurlcacheentryfile.htm
tech.root: wininet
ms.assetid: eb311b8d-560d-4742-af4c-b5afe660c8e5
ms.date: 12/05/2018
ms.keywords: RetrieveUrlCacheEntryFile, RetrieveUrlCacheEntryFile function [WinINet], RetrieveUrlCacheEntryFileA, RetrieveUrlCacheEntryFileW, _inet_retrieveurlcacheentryfile_function, wininet.retrieveurlcacheentryfile, wininet/RetrieveUrlCacheEntryFile, wininet/RetrieveUrlCacheEntryFileA, wininet/RetrieveUrlCacheEntryFileW
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RetrieveUrlCacheEntryFileW (Unicode) and RetrieveUrlCacheEntryFileA (ANSI)
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
 - RetrieveUrlCacheEntryFileW
 - wininet/RetrieveUrlCacheEntryFileW
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
 - RetrieveUrlCacheEntryFile
 - RetrieveUrlCacheEntryFileA
 - RetrieveUrlCacheEntryFileW
---

# RetrieveUrlCacheEntryFileW function


## -description

Locks the cache entry file associated with the specified URL.

## -parameters

### -param lpszUrlName [in]

Pointer to a string that contains the URL of the resource associated with the cache entry. This must be a unique name. The name string should not contain any escape characters.

### -param lpCacheEntryInfo [out]

Pointer to a cache entry information buffer. If the buffer is not sufficient, this function returns ERROR_INSUFFICIENT_BUFFER and sets 
<i>lpdwCacheEntryInfoBufferSize</i> to the number of bytes required.

### -param lpcbCacheEntryInfo [in, out]

Pointer to an unsigned long integer variable that specifies the size of the 
<i>lpCacheEntryInfo</i> buffer, in bytes. When the function returns, the variable contains the size, in bytes, of the actual buffer used or the number of bytes required to retrieve the cache entry file. The caller should check the return value in this parameter. If the return size is less than or equal to the size passed in, all the relevant data has been returned.

### -param dwReserved [in]

This parameter is reserved and must be 0.

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Possible error values include:

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
The size of the 
<i>lpCacheEntryInfo</i> buffer as specified by 
<i>lpdwCacheEntryInfoBufferSize</i> is not sufficient to contain all the information. The value returned in 
<i>lpdwCacheEntryInfoBufferSize</i> indicates the buffer size necessary to get all the information.

</td>
</tr>
</table>

## -remarks

<b>RetrieveUrlCacheEntryFile</b> does not do any URL parsing, so a URL containing an anchor (#) will not be found in the cache, even if the resource is cached. For example, if the URL http://adatum.com/example.htm#sample was passed, the function would return ERROR_FILE_NOT_FOUND even if http://adatum.com/example.htm is in the cache.

The file is locked for the caller when it is retrieved; the caller should unlock the file after the caller is finished with the file. The cache manager automatically unlocks the files after a certain interval. While the file is locked, the cache manager will not remove the file from the cache. It is important to note that this function may or may not perform efficiently, depending on the internal implementation of the cache. For instance, if the URL data is stored in a packed file that contains data for other URLs, the cache will make a copy of the data to a file in a temporary directory maintained by the cache. The cache will eventually delete the copy. It is recommended that this function be used only in situations where a file name is needed to launch an application. 
<a href="/windows/desktop/api/wininet/nf-wininet-retrieveurlcacheentrystreama">RetrieveUrlCacheEntryStream</a> and associated stream functions should be used in most cases.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines RetrieveUrlCacheEntryFile as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/caching">Caching</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
