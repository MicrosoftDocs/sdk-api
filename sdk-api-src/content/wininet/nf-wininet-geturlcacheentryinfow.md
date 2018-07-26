---
UID: NF:wininet.GetUrlCacheEntryInfoW
title: GetUrlCacheEntryInfoW function
author: windows-sdk-content
description: Retrieves information about a cache entry.
old-location: wininet\geturlcacheentryinfo.htm
old-project: wininet
ms.assetid: 0f70bcef-2d56-4765-a44e-4549b4ae2ced
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: GetUrlCacheEntryInfo, GetUrlCacheEntryInfo function [WinINet], GetUrlCacheEntryInfoA, GetUrlCacheEntryInfoW, _inet_geturlcacheentryinfo_function, wininet.geturlcacheentryinfo, wininet/GetUrlCacheEntryInfo, wininet/GetUrlCacheEntryInfoA, wininet/GetUrlCacheEntryInfoW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetUrlCacheEntryInfoW (Unicode) and GetUrlCacheEntryInfoA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: InternetCookieState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wininet.dll
api_name:
 - GetUrlCacheEntryInfo
 - GetUrlCacheEntryInfoA
 - GetUrlCacheEntryInfoW
product: Windows
targetos: Windows
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetUrlCacheEntryInfoW function


## -description


Retrieves information about a cache entry.


## -parameters




### -param lpszUrlName [in]

A pointer to a null-terminated string that contains the name of the cache entry. The name string should not contain any escape characters.


### -param lpCacheEntryInfo [out]

A pointer to an 
<a href="https://msdn.microsoft.com/7bda08e0-5df0-4087-a5cd-3a25c6ae5ade">INTERNET_CACHE_ENTRY_INFO</a> structure that receives information about the cache entry. A buffer should be allocated for this parameter. 

Since the required size of the buffer is not known in advance,  it is best to allocate a buffer adequate to handle the size of most <a href="https://msdn.microsoft.com/7bda08e0-5df0-4087-a5cd-3a25c6ae5ade">INTERNET_CACHE_ENTRY_INFO</a> entries. There is no cache entry size limit, so applications that need to enumerate the cache must be prepared to allocate variable-sized buffers.


### -param lpcbCacheEntryInfo [in, out]

A pointer to a variable that specifies the size of the 
<i>lpCacheEntryInfo</i> buffer, in bytes. When the function returns, the variable contains the number of bytes copied to the buffer, or the required size of the buffer, in bytes.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Possible error values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified cache entry is not found in the cache.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The size of 
<i>lpCacheEntryInfo</i> as specified by 
<i>lpdwCacheEntryInfoBufferSize</i> is not sufficient to contain all the information. The value returned in 
<i>lpdwCacheEntryInfoBufferSize</i> indicates the buffer size necessary to contain all the information.

</td>
</tr>
</table>
 




## -remarks



<b>GetUrlCacheEntryInfo</b> does not do any URL parsing, so a URL containing an anchor (#) will not be found in the cache, even if the resource is cached. For example, if the URL http://example.com/example.htm#sample is passed, the function returns <b>ERROR_FILE_NOT_FOUND</b> even if http://example.com/example.htm is in the cache.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/44c268c9-a745-432a-8540-60d7e7d2cb2d">Caching</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97"> WinINet Functions</a>
 

 

