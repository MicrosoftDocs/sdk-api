---
UID: NF:wininet.FindNextUrlCacheEntryA
title: FindNextUrlCacheEntryA function (wininet.h)
description: Retrieves the next entry in the Internet cache.
helpviewer_keywords: ["FindNextUrlCacheEntry","FindNextUrlCacheEntry function [WinINet]","FindNextUrlCacheEntryA","FindNextUrlCacheEntryW","_inet_findnexturlcacheentry_function","wininet.findnexturlcacheentry","wininet/FindNextUrlCacheEntry","wininet/FindNextUrlCacheEntryA","wininet/FindNextUrlCacheEntryW"]
old-location: wininet\findnexturlcacheentry.htm
tech.root: wininet
ms.assetid: 776bf73e-00f3-46a1-a8c7-5eb365e9a518
ms.date: 12/05/2018
ms.keywords: FindNextUrlCacheEntry, FindNextUrlCacheEntry function [WinINet], FindNextUrlCacheEntryA, FindNextUrlCacheEntryW, _inet_findnexturlcacheentry_function, wininet.findnexturlcacheentry, wininet/FindNextUrlCacheEntry, wininet/FindNextUrlCacheEntryA, wininet/FindNextUrlCacheEntryW
f1_keywords:
- wininet/FindNextUrlCacheEntry
dev_langs:
- c++
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FindNextUrlCacheEntryW (Unicode) and FindNextUrlCacheEntryA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Wininet.dll
api_name:
- FindNextUrlCacheEntry
- FindNextUrlCacheEntryA
- FindNextUrlCacheEntryW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FindNextUrlCacheEntryA function


## -description


Retrieves the next entry in the Internet cache.


## -parameters




### -param hEnumHandle [in]

Handle to the enumeration obtained from a previous call to 
<a href="https://docs.microsoft.com/windows/desktop/api/wininet/nf-wininet-findfirsturlcacheentrya">FindFirstUrlCacheEntry</a>.


### -param lpNextCacheEntryInfo [out]

Pointer to an 
<a href="https://docs.microsoft.com/windows/desktop/api/wininet/ns-wininet-internet_cache_entry_infoa">INTERNET_CACHE_ENTRY_INFO</a> structure that receives information about the cache entry.


### -param lpcbCacheEntryInfo [in, out]

Pointer to a variable that specifies the size of the 
<i>lpNextCacheEntryInfo</i> buffer, in bytes. When the function returns, the variable contains the number of bytes copied to the buffer, or the size of the buffer required to retrieve the cache entry, in bytes.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Possible error values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The size of 
<i>lpNextCacheEntryInfo</i> as specified by 
<i>lpdwNextCacheEntryInfoBufferSize</i> is not sufficient to contain all the information. The value returned in 
<i>lpdwNextCacheEntryInfoBufferSize</i> indicates the buffer size necessary to contain all the information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
The enumeration completed.

</td>
</tr>
</table>
 




## -remarks



Continue to call <b>FindNextUrlCacheEntry</b> until the last item in the cache is returned. 

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://docs.microsoft.com/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines FindNextUrlCacheEntry as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinInet/caching">Caching</a>



<a href="https://docs.microsoft.com/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
 

 

