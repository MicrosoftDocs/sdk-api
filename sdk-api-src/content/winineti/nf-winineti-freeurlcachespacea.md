---
UID: NF:winineti.FreeUrlCacheSpaceA
title: FreeUrlCacheSpaceA function (winineti.h)
description: Frees space in the cache. (ANSI)
helpviewer_keywords: ["FreeUrlCacheSpaceA", "winineti/FreeUrlCacheSpaceA"]
old-location: wininet\freeurlcachespace.htm
tech.root: wininet
ms.assetid: 5853CA64-551F-484E-A992-25B9EA6C74C2
ms.date: 12/05/2018
ms.keywords: FreeUrlCacheSpace, FreeUrlCacheSpace function [WinINet], FreeUrlCacheSpaceA, FreeUrlCacheSpaceW, wininet.freeurlcachespace, winineti/FreeUrlCacheSpace, winineti/FreeUrlCacheSpaceA, winineti/FreeUrlCacheSpaceW
req.header: winineti.h
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
 - FreeUrlCacheSpaceA
 - winineti/FreeUrlCacheSpaceA
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
 - FreeUrlCacheSpace
 - FreeUrlCacheSpaceA
 - FreeUrlCacheSpaceW
---

# FreeUrlCacheSpaceA function


## -description



Frees space in the cache.<div class="alert"><b>Note</b>  This API is deprecated. Please use the <a href="/previous-versions/windows/desktop/Gg269259(v=EXCHG.10)">Extensible Storage Engine</a> instead.</div>
<div> </div>

## -parameters

### -param lpszCachePath

The path for the cache.

### -param dwSize

The percentage of the cache to free (in the range 1 to 100, inclusive).

### -param dwFilter [in]

This parameter is reserved, and must be 0.

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service nor when impersonating a security context. For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The winineti.h header defines FreeUrlCacheSpace as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/caching">Caching</a>



<a href="/windows/desktop/api/winineti/nf-winineti-createurlcachecontainera">CreateUrlCacheContainer</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
