---
UID: NF:wininet.CreateUrlCacheEntryW
title: CreateUrlCacheEntryW function (wininet.h)
description: Creates a local file name for saving the cache entry based on the specified URL and the file name extension. (Unicode)
helpviewer_keywords: ["CreateUrlCacheEntry", "CreateUrlCacheEntry function [WinINet]", "CreateUrlCacheEntryW", "_inet_createurlcacheentry_function", "wininet.createurlcacheentry", "wininet/CreateUrlCacheEntry", "wininet/CreateUrlCacheEntryW"]
old-location: wininet\createurlcacheentry.htm
tech.root: wininet
ms.assetid: 9a58cf05-2306-4a0f-876d-85f5e91c5a2b
ms.date: 12/05/2018
ms.keywords: CreateUrlCacheEntry, CreateUrlCacheEntry function [WinINet], CreateUrlCacheEntryA, CreateUrlCacheEntryW, _inet_createurlcacheentry_function, wininet.createurlcacheentry, wininet/CreateUrlCacheEntry, wininet/CreateUrlCacheEntryA, wininet/CreateUrlCacheEntryW
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreateUrlCacheEntryW (Unicode) and CreateUrlCacheEntryA (ANSI)
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
 - CreateUrlCacheEntryW
 - wininet/CreateUrlCacheEntryW
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
 - CreateUrlCacheEntry
 - CreateUrlCacheEntryA
 - CreateUrlCacheEntryW
---

# CreateUrlCacheEntryW function


## -description

Creates a local file name for saving the cache entry based on the specified URL and the file name extension.

## -parameters

### -param lpszUrlName [in]

Pointer to a string value that contains the name of the URL. The string must contain a value; an empty string will cause <b>CreateUrlCacheEntry</b> to fail. In addition, the string must not contain any escape characters.

### -param dwExpectedFileSize [in]

Expected size of the file needed to store the data that corresponds to the source entity, in <b>TCHARs</b>. If the expected size is unknown, set this value to zero.

### -param lpszFileExtension [in]

Pointer to a string value that contains an extension name of the file in the local storage.

### -param lpszFileName [out]

Pointer to a buffer that receives the file name. The buffer should be large enough  to store the path of the created file (at least MAX_PATH  characters in length).

### -param dwReserved [in]

This parameter is reserved and must be 0.

## -returns

If the function succeeds, the function returns <b>TRUE</b>.


If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

After 
<b>CreateUrlCacheEntry</b> is called, the application can write directly into the file in local storage. When the file is completely received, the caller should call 
<a href="/windows/desktop/api/wininet/nf-wininet-commiturlcacheentrya">CommitUrlCacheEntry</a> to commit the entry in the cache.

WinINet attempts to decode Unicode  parameters according to the system code page. Applications should ensure that  Unicode parameters are properly encoded for the system code page. Applications can set the system code page with <a href="/windows/desktop/api/wininet/nf-wininet-internetsetoptiona">InternetSetOption</a> as shown in the following code example:


``` syntax
DWORD CP_SHIFT_JIS = 932;  // ANSI/OEM  Japanese, Shift-JIS
InternetSetOption( hRequest, 
                   INTERNET_OPTION_CODEPAGE,
                   &CP_SHIFT_JIS,
                   sizeof(DWORD) );
```

If the Unicode parameter is not properly encoded to the system code page, WinINet attempts UTF8 decoding. 

When items are retrieved from the cache, the system code page that was used to place the item in the cache must match the current system code page for the user. For applications running under IE6 and earlier, if decoding for the system code page fails, WinINet attempts UTF8 decoding. 

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines CreateUrlCacheEntry as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/caching">Caching</a>



<a href="/windows/desktop/api/wininet/nf-wininet-commiturlcacheentrya">CommitUrlCacheEntry</a>



<a href="/windows/desktop/WinInet/wininet-functions"> WinINet Functions</a>
