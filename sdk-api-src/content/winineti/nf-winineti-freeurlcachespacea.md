---
UID: NF:winineti.FreeUrlCacheSpaceA
title: FreeUrlCacheSpaceA function (winineti.h)
description: Frees space in the cache.
old-location: wininet\freeurlcachespace.htm
tech.root: wininet
ms.assetid: 5853CA64-551F-484E-A992-25B9EA6C74C2
ms.date: 12/05/2018
ms.keywords: FreeUrlCacheSpace, FreeUrlCacheSpace function [WinINet], FreeUrlCacheSpaceA, FreeUrlCacheSpaceW, wininet.freeurlcachespace, winineti/FreeUrlCacheSpace, winineti/FreeUrlCacheSpaceA, winineti/FreeUrlCacheSpaceW
ms.topic: function
f1_keywords:
- winineti/FreeUrlCacheSpace
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FreeUrlCacheSpaceA function


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Frees space in the cache.<div class="alert"><b>Note</b>  This API is deprecated. Please use the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/Gg269259(v=EXCHG.10)">Extensible Storage Engine</a> instead.</div>
<div> </div>



## -parameters




### -param lpszCachePath

The path for the cache.


### -param dwSize

The percentage of the cache to free (in the range 1 to 100, inclusive).


### -param dwFilter [in]

This parameter is reserved, and must be 0.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service nor when impersonating a security context. For server implementations or services use <a href="https://docs.microsoft.com/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinInet/caching">Caching</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winineti/nf-winineti-createurlcachecontainera">CreateUrlCacheContainer</a>



<a href="https://docs.microsoft.com/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
 

 

