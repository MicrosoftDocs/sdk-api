---
UID: NF:wininet.FindFirstUrlCacheGroup
title: FindFirstUrlCacheGroup function (wininet.h)
description: Initiates the enumeration of the cache groups in the Internet cache.
helpviewer_keywords: ["FindFirstUrlCacheGroup","FindFirstUrlCacheGroup function [WinINet]","_inet_findfirsturlcachegroup_function","wininet.findfirsturlcachegroup","wininet/FindFirstUrlCacheGroup"]
old-location: wininet\findfirsturlcachegroup.htm
tech.root: wininet
ms.assetid: a333cbc6-a880-4b1c-be0d-abb083909638
ms.date: 12/05/2018
ms.keywords: FindFirstUrlCacheGroup, FindFirstUrlCacheGroup function [WinINet], _inet_findfirsturlcachegroup_function, wininet.findfirsturlcachegroup, wininet/FindFirstUrlCacheGroup
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
 - FindFirstUrlCacheGroup
 - wininet/FindFirstUrlCacheGroup
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
 - FindFirstUrlCacheGroup
---

# FindFirstUrlCacheGroup function


## -description

Initiates the enumeration of the cache groups in the Internet cache.

## -parameters

### -param dwFlags [in]

This parameter is reserved and must be 0.

### -param dwFilter [in]

Filters to be used. This parameter can be zero or one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>CACHEGROUP_SEARCH_ALL</dt>
</dl>
</td>
<td width="60%">
Search all  cache groups.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>CACHEGROUP_SEARCH_BYURL</dt>
</dl>
</td>
<td width="60%">
Not currently implemented.

</td>
</tr>
</table>

### -param lpSearchCondition [in]

This parameter is reserved and must be <b>NULL</b>.

### -param dwSearchCondition [in]

This parameter is reserved and must be 0.

### -param lpGroupId [out]

Pointer to the ID of the first cache group that matches the search criteria.

### -param lpReserved [in, out]

This parameter is reserved and must be <b>NULL</b>.

## -returns

Returns a valid handle to the first item in the enumeration if successful, or <b>NULL</b> otherwise. To get specific error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. If the function finds no matching files, 
<b>GetLastError</b> returns ERROR_NO_MORE_FILES.

## -remarks

The handle returned from <b>FindFirstUrlCacheGroup</b> is used in subsequent calls to <a href="/windows/desktop/api/wininet/nf-wininet-findnexturlcachegroup">FindNextUrlCacheGroup</a>. At the end of the enumeration, the application should call 
<a href="/windows/desktop/api/wininet/nf-wininet-findcloseurlcache">FindCloseUrlCache</a>.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/WinInet/caching">Caching</a>



<a href="/windows/desktop/WinInet/wininet-functions"> WinINet Functions</a>