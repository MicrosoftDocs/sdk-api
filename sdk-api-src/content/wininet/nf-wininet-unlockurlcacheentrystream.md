---
UID: NF:wininet.UnlockUrlCacheEntryStream
title: UnlockUrlCacheEntryStream function (wininet.h)
description: Closes the stream that has been retrieved using the RetrieveUrlCacheEntryStream function.
helpviewer_keywords: ["UnlockUrlCacheEntryStream","UnlockUrlCacheEntryStream function [WinINet]","_inet_unlockurlcacheentrystream_function","wininet.unlockurlcacheentrystream","wininet/UnlockUrlCacheEntryStream"]
old-location: wininet\unlockurlcacheentrystream.htm
tech.root: wininet
ms.assetid: 9fcc257e-732c-4545-a81b-7db20a98e497
ms.date: 12/05/2018
ms.keywords: UnlockUrlCacheEntryStream, UnlockUrlCacheEntryStream function [WinINet], _inet_unlockurlcacheentrystream_function, wininet.unlockurlcacheentrystream, wininet/UnlockUrlCacheEntryStream
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
 - UnlockUrlCacheEntryStream
 - wininet/UnlockUrlCacheEntryStream
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
 - UnlockUrlCacheEntryStream
---

# UnlockUrlCacheEntryStream function


## -description

Closes the stream that has been retrieved using the 
<a href="/windows/desktop/api/wininet/nf-wininet-retrieveurlcacheentrystreama">RetrieveUrlCacheEntryStream</a> function.

## -parameters

### -param hUrlCacheStream [in]

Handle that was returned by the 
<a href="/windows/desktop/api/wininet/nf-wininet-retrieveurlcacheentrystreama">RetrieveUrlCacheEntryStream</a> function.

### -param Reserved [in]

This parameter is reserved and must be <b>NULL</b>.

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/WinInet/caching">Caching</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>