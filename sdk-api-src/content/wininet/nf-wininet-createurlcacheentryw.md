---
UID: NF:wininet.CreateUrlCacheEntryW
title: CreateUrlCacheEntryW function
author: windows-sdk-content
description: Creates a local file name for saving the cache entry based on the specified URL and the file name extension.
old-location: wininet\createurlcacheentry.htm
tech.root: WinInet
ms.assetid: 9a58cf05-2306-4a0f-876d-85f5e91c5a2b
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CreateUrlCacheEntry, CreateUrlCacheEntry function [WinINet], CreateUrlCacheEntryA, CreateUrlCacheEntryW, _inet_createurlcacheentry_function, wininet.createurlcacheentry, wininet/CreateUrlCacheEntry, wininet/CreateUrlCacheEntryA, wininet/CreateUrlCacheEntryW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- CreateUrlCacheEntryW
: 
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
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



After 
<b>CreateUrlCacheEntry</b> is called, the application can write directly into the file in local storage. When the file is completely received, the caller should call 
<a href="https://msdn.microsoft.com/4bd21b30-cac5-482b-9826-b5a4ffeeebe9">CommitUrlCacheEntry</a> to commit the entry in the cache.

WinINet attempts to decode Unicode  parameters according to the system code page. Applications should ensure that  Unicode parameters are properly encoded for the system code page. Applications can set the system code page with <a href="https://msdn.microsoft.com/578c7130-7426-4a2e-ae0f-ed8a84449b06">InternetSetOption</a> as shown in the following code example:

<pre class="syntax" xml:space="preserve"><code>DWORD CP_SHIFT_JIS = 932;  // ANSI/OEM  Japanese, Shift-JIS
InternetSetOption( hRequest, 
                   INTERNET_OPTION_CODEPAGE,
                   &amp;CP_SHIFT_JIS, 
                   sizeof(DWORD) );</code></pre>
If the Unicode parameter is not properly encoded to the system code page, WinINet attempts UTF8 decoding. 

When items are retrieved from the cache, the system code page that was used to place the item in the cache must match the current system code page for the user. For applications running under IE6 and earlier, if decoding for the system code page fails, WinINet attempts UTF8 decoding. 

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/44c268c9-a745-432a-8540-60d7e7d2cb2d">Caching</a>



<a href="https://msdn.microsoft.com/4bd21b30-cac5-482b-9826-b5a4ffeeebe9">CommitUrlCacheEntry</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97"> WinINet Functions</a>
 

 

