---
UID: NF:wininet.FindFirstUrlCacheEntryW
title: FindFirstUrlCacheEntryW function
author: windows-driver-content
description: Begins the enumeration of the Internet cache.
old-location: wininet\findfirsturlcacheentry.htm
old-project: WinInet
ms.assetid: e8407284-846b-4080-b75b-4805330e0f95
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: FindFirstUrlCacheEntry, FindFirstUrlCacheEntry function [WinINet], FindFirstUrlCacheEntryA, FindFirstUrlCacheEntryW, _inet_findfirsturlcacheentry_function, wininet.findfirsturlcacheentry, wininet/FindFirstUrlCacheEntry, wininet/FindFirstUrlCacheEntryA, wininet/FindFirstUrlCacheEntryW
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
req.unicode-ansi: FindFirstUrlCacheEntryW (Unicode) and FindFirstUrlCacheEntryA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: InternetCookieState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wininet.dll
api_name:
-	FindFirstUrlCacheEntry
-	FindFirstUrlCacheEntryA
-	FindFirstUrlCacheEntryW
product: Windows
targetos: Windows
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# FindFirstUrlCacheEntryW function


## -description


Begins the enumeration of the Internet cache.


## -parameters




### -param lpszUrlSearchPattern [in]

A pointer to a string that contains the source name pattern to search for. This parameter can only be set to "cookie:", "visited:", or <b>NULL</b>. Set this parameter to "cookie:" to enumerate the cookies or "visited:" to enumerate the URL History entries in the cache. If this parameter is <b>NULL</b>, <b>FindFirstUrlCacheEntry</b> returns all content entries in the cache.


### -param lpFirstCacheEntryInfo [out]

Pointer to an 
<a href="https://msdn.microsoft.com/7bda08e0-5df0-4087-a5cd-3a25c6ae5ade">INTERNET_CACHE_ENTRY_INFO</a> structure.


### -param lpcbCacheEntryInfo [in, out]

Pointer to a variable that specifies the size of the 
<i>lpFirstCacheEntryInfo</i> buffer, in bytes. When the function returns, the variable contains the number of bytes copied to the buffer, or the required size needed to retrieve the cache entry, in bytes.


## -returns



Returns a handle that the application can use in the 
<a href="https://msdn.microsoft.com/776bf73e-00f3-46a1-a8c7-5eb365e9a518">FindNextUrlCacheEntry</a> function to retrieve subsequent entries in the cache. If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

ERROR_INSUFFICIENT_BUFFER indicates that the size of 
<i>lpFirstCacheEntryInfo</i> as specified by 
<i>lpdwFirstCacheEntryInfoBufferSize</i> is not sufficient to contain all the information. The value returned in 
<i>lpdwFirstCacheEntryInfoBufferSize</i> indicates the buffer size necessary to contain all the information.




## -remarks



The handle returned from <b>FindFirstUrlCacheEntry</b> is used in all subsequent calls to <a href="https://msdn.microsoft.com/776bf73e-00f3-46a1-a8c7-5eb365e9a518">FindNextUrlCacheEntry</a>. At the end of the enumeration, the application should call 
<a href="https://msdn.microsoft.com/54fc7bea-4cc1-4034-93c3-49ec88817648">FindCloseUrlCache</a>.

<b>FindFirstUrlCacheEntry</b> and 
<a href="https://msdn.microsoft.com/776bf73e-00f3-46a1-a8c7-5eb365e9a518">FindNextUrlCacheEntry</a> return variable size information. If ERROR_INSUFFICIENT_BUFFER is returned, the application should allocate a buffer of the size specified by 
<i>lpdwFirstCacheEntryInfoBufferSize</i>. For more information, see 
<a href="https://msdn.microsoft.com/ae7f84ba-15d4-483b-bdda-0042854f9e1b">Using Buffers</a>.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/44c268c9-a745-432a-8540-60d7e7d2cb2d">Caching</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97"> WinINet Functions</a>
 

 

