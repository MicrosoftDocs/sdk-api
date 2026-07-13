---
UID: NF:wininet.GetUrlCacheEntryInfoExA
title: GetUrlCacheEntryInfoExA function (wininet.h)
description: Retrieves information on the cache entry associated with the specified URL, taking into account any redirections that are applied in offline mode by the HttpSendRequest function. (ANSI)
helpviewer_keywords: ["GetUrlCacheEntryInfoExA", "wininet/GetUrlCacheEntryInfoExA"]
old-location: wininet\geturlcacheentryinfoex.htm
tech.root: wininet
ms.assetid: 3842dae9-9474-492a-83fa-29d7927dc92d
ms.date: 12/05/2018
ms.keywords: GetUrlCacheEntryInfoEx, GetUrlCacheEntryInfoEx function [WinINet], GetUrlCacheEntryInfoExA, GetUrlCacheEntryInfoExW, _inet_geturlcacheentryinfoex_function, wininet.geturlcacheentryinfoex, wininet/GetUrlCacheEntryInfoEx, wininet/GetUrlCacheEntryInfoExA, wininet/GetUrlCacheEntryInfoExW
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetUrlCacheEntryInfoExW (Unicode) and GetUrlCacheEntryInfoExA (ANSI)
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
 - GetUrlCacheEntryInfoExA
 - wininet/GetUrlCacheEntryInfoExA
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
 - GetUrlCacheEntryInfoEx
 - GetUrlCacheEntryInfoExA
 - GetUrlCacheEntryInfoExW
---

# GetUrlCacheEntryInfoExA function


## -description

Retrieves information on the cache entry associated with the specified URL, taking into account any redirections that are applied in offline mode by the 
<a href="/windows/desktop/api/wininet/nf-wininet-httpsendrequesta">HttpSendRequest</a> function.

## -parameters

### -param lpszUrl [in]

A pointer to a <b>null</b>-terminated string that contains the name of the cache entry. The name string should not contain any escape characters.

### -param lpCacheEntryInfo [in, out, optional]

A pointer to an 
<a href="/windows/desktop/api/wininet/ns-wininet-internet_cache_entry_infoa">INTERNET_CACHE_ENTRY_INFO</a> structure that receives information about the cache entry. A buffer should be allocated for this parameter. 

Since the required size of the buffer is not known in advance,  it is best to allocate a buffer adequate to handle the size of most <a href="/windows/desktop/api/wininet/ns-wininet-internet_cache_entry_infoa">INTERNET_CACHE_ENTRY_INFO</a> entries. There is no cache entry size limit, so applications that need to enumerate the cache must be prepared to allocate variable-sized buffers.

### -param lpcbCacheEntryInfo [in, out, optional]

Pointer to a variable that specifies the size of the 
<i>lpCacheEntryInfo</i> buffer, in bytes. When the function returns, the variable contains the number of bytes copied to the buffer, or the required size of the buffer in bytes.

### -param lpszRedirectUrl [out]

This parameter is reserved and must be <b>NULL</b>.

### -param lpcbRedirectUrl [in, out]

This parameter is reserved and must be <b>NULL</b>.

### -param lpReserved

This parameter is reserved and must be <b>NULL</b>.

### -param dwFlags [in]

This parameter is reserved and must be 0.

## -returns

Returns <b>TRUE</b> if the URL was located, or <b>FALSE</b> otherwise. Call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> for specific error information. Possible errors include the following.

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
The URL was not found in the cache index, even after taking any cached redirections into account.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer referenced by 
<i>lpCacheEntryInfo</i> was not large enough to hold the requested information. The size of the buffer needed will be returned to 
<i>lpdwCacheEntryInfoBufSize</i>.

</td>
</tr>
</table>

## -remarks

<b>GetUrlCacheEntryInfoEx</b> does not do any URL parsing, so a URL containing an anchor (#) will not be found in the cache, even if the resource is cached. For example, if the URL `http://example.com/example.htm#sample` is passed, the function returns ERROR_FILE_NOT_FOUND even if `http://example.com/example.htm` is in the cache.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines GetUrlCacheEntryInfoEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/caching">Caching</a>



<a href="/windows/desktop/WinInet/wininet-functions"> WinINet Functions</a>
