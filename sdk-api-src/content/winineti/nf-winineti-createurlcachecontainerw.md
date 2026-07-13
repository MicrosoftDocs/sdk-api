---
UID: NF:winineti.CreateUrlCacheContainerW
title: CreateUrlCacheContainerW function (winineti.h)
description: Creates a cache container in the specified cache path to hold cache entries based on the specified name, cache prefix, and container type. (Unicode)
helpviewer_keywords: ["CreateUrlCacheContainer", "CreateUrlCacheContainer function [WinINet]", "CreateUrlCacheContainerW", "wininet.createurlcachecontainer", "winineti/CreateUrlCacheContainer"]
old-location: wininet\createurlcachecontainer.htm
tech.root: wininet
ms.assetid: 19b518cc-2f02-49c3-bedc-f5d633cc635d
ms.date: 12/05/2018
ms.keywords: CreateUrlCacheContainer, CreateUrlCacheContainer function [WinINet], CreateUrlCacheContainerA, CreateUrlCacheContainerW, wininet.createurlcachecontainer, winineti/CreateUrlCacheContainer
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
 - CreateUrlCacheContainerW
 - winineti/CreateUrlCacheContainerW
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
 - CreateUrlCacheContainer
---

# CreateUrlCacheContainerW function


## -description

Creates a cache container in the specified cache path to hold cache entries based on the specified name, cache prefix, and container type.
<div class="alert"><b>Note</b>  Note: This API is deprecated. Please use the <a href="/previous-versions/windows/desktop/Gg269259(v=EXCHG.10)">Extensible Storage Engine</a> instead.</div><div> </div>

## -parameters

### -param Name [in]

The name to give to the cache.

### -param lpCachePrefix [in]

The cache prefix to base the cache on.

### -param lpszCachePath [in, optional]

The cache prefix to create the cache in.

### -param KBCacheLimit [in]

The size limit of the cache in whole kilobytes, or 0 for the default size.

### -param dwContainerType [in]

The container type to base the cache on.

### -param dwOptions [in]

This parameter is reserved and must be 0.

### -param pvBuffer

This parameter is reserved and must be <b>NULL</b>.

### -param cbBuffer [in, out]

This parameter is reserved and must be <b>NULL</b>.

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/WinInet/caching">Caching</a>



<a href="/windows/desktop/api/wininet/nf-wininet-commiturlcacheentryw">CommitUrlCacheEntry</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>

## -remarks

> [!NOTE]
> The winineti.h header defines CreateUrlCacheContainer as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
