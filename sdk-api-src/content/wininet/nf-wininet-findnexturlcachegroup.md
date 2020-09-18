---
UID: NF:wininet.FindNextUrlCacheGroup
title: FindNextUrlCacheGroup function (wininet.h)
description: Retrieves the next cache group in a cache group enumeration started by FindFirstUrlCacheGroup.
helpviewer_keywords: ["FindNextUrlCacheGroup","FindNextUrlCacheGroup function [WinINet]","_inet_findnexturlcachegroup_function","wininet.findnexturlcachegroup","wininet/FindNextUrlCacheGroup"]
old-location: wininet\findnexturlcachegroup.htm
tech.root: wininet
ms.assetid: f3cbe67c-c069-404c-8ca4-d18b35cc4c4a
ms.date: 12/05/2018
ms.keywords: FindNextUrlCacheGroup, FindNextUrlCacheGroup function [WinINet], _inet_findnexturlcachegroup_function, wininet.findnexturlcachegroup, wininet/FindNextUrlCacheGroup
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
 - FindNextUrlCacheGroup
 - wininet/FindNextUrlCacheGroup
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
 - FindNextUrlCacheGroup
---

# FindNextUrlCacheGroup function


## -description

Retrieves the next cache group in a cache group enumeration started by 
<a href="/windows/desktop/api/wininet/nf-wininet-findfirsturlcachegroup">FindFirstUrlCacheGroup</a>.

## -parameters

### -param hFind [in]

The cache group enumeration handle, which is returned by 
<a href="/windows/desktop/api/wininet/nf-wininet-findfirsturlcachegroup">FindFirstUrlCacheGroup</a>.

### -param lpGroupId [out]

Pointer to a variable that receives the cache group identifier.

### -param lpReserved [in, out]

This parameter is reserved and must be <b>NULL</b>.

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get specific error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Continue to call <b>FindNextUrlCacheGroup</b> until the last item in the cache is returned.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/WinInet/caching">Caching</a>



<a href="/windows/desktop/WinInet/wininet-functions"> WinINet Functions</a>