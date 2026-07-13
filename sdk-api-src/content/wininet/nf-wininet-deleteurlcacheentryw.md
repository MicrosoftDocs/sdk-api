---
UID: NF:wininet.DeleteUrlCacheEntryW
title: DeleteUrlCacheEntryW function (wininet.h)
description: The DeleteUrlCacheEntryW (Unicode) function (wininet.h) removes the file associated with the source name from the cache, if the file exists.
helpviewer_keywords: ["DeleteUrlCacheEntry", "DeleteUrlCacheEntry function [WinINet]", "DeleteUrlCacheEntryW", "_inet_deleteurlcacheentry_function", "wininet.deleteurlcacheentry", "wininet/DeleteUrlCacheEntry", "wininet/DeleteUrlCacheEntryW"]
old-location: wininet\deleteurlcacheentry.htm
tech.root: wininet
ms.assetid: bb765cba-6662-4dca-8f9f-3f35e37da28a
ms.date: 08/10/2022
ms.keywords: DeleteUrlCacheEntry, DeleteUrlCacheEntry function [WinINet], DeleteUrlCacheEntryA, DeleteUrlCacheEntryW, _inet_deleteurlcacheentry_function, wininet.deleteurlcacheentry, wininet/DeleteUrlCacheEntry, wininet/DeleteUrlCacheEntryA, wininet/DeleteUrlCacheEntryW
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DeleteUrlCacheEntryW (Unicode) and DeleteUrlCacheEntryA (ANSI)
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
 - DeleteUrlCacheEntryW
 - wininet/DeleteUrlCacheEntryW
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
 - DeleteUrlCacheEntry
 - DeleteUrlCacheEntryA
 - DeleteUrlCacheEntryW
---

# DeleteUrlCacheEntryW function


## -description

Removes the file associated with the source name from the cache, if the file exists.

## -parameters

### -param lpszUrlName [in]

Pointer to a string that contains the name of the source that corresponds to the cache entry.

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Possible error values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The file is locked or in use. The entry is marked and  deleted when the file is unlocked.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The file is not in the cache.

</td>
</tr>
</table>

## -remarks

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines DeleteUrlCacheEntry as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/caching">Caching</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
