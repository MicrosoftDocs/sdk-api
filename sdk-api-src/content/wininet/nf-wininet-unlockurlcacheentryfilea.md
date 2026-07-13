---
UID: NF:wininet.UnlockUrlCacheEntryFileA
title: UnlockUrlCacheEntryFileA function (wininet.h)
description: Unlocks the cache entry that was locked while the file was retrieved for use from the cache. (UnlockUrlCacheEntryFileA)
helpviewer_keywords: ["UnlockUrlCacheEntryFileA", "wininet/UnlockUrlCacheEntryFileA"]
old-location: wininet\unlockurlcacheentryfile.htm
tech.root: wininet
ms.assetid: ccc650dc-1759-4438-85d5-539c71d21a74
ms.date: 12/05/2018
ms.keywords: UnlockUrlCacheEntryFile, UnlockUrlCacheEntryFile function [WinINet], UnlockUrlCacheEntryFileA, UnlockUrlCacheEntryFileW, _inet_unlockurlcacheentryfile_function, wininet.unlockurlcacheentryfile, wininet/UnlockUrlCacheEntryFile, wininet/UnlockUrlCacheEntryFileA, wininet/UnlockUrlCacheEntryFileW
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: UnlockUrlCacheEntryFileW (Unicode) and UnlockUrlCacheEntryFileA (ANSI)
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
 - UnlockUrlCacheEntryFileA
 - wininet/UnlockUrlCacheEntryFileA
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
 - UnlockUrlCacheEntryFile
 - UnlockUrlCacheEntryFileA
 - UnlockUrlCacheEntryFileW
---

# UnlockUrlCacheEntryFileA function


## -description

Unlocks the cache entry that was locked while the file was retrieved for use from the cache.

## -parameters

### -param lpszUrlName [in]

Pointer to a <b>null</b>-terminated string that specifies the source name of the cache entry that is being unlocked. The name string should not contain any escape characters.

### -param dwReserved [in]

This parameter is reserved and must be 0.

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. ERROR_FILE_NOT_FOUND indicates that the cache entry specified by the source name is not found in the cache storage.

## -remarks

The application should not access the file after calling this function.

When this function returns, the cache manager is free to delete the cache entry.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines UnlockUrlCacheEntryFile as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/caching">Caching</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
