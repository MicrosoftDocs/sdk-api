---
UID: NF:wininet.FindNextUrlCacheEntryW
title: FindNextUrlCacheEntryW function
author: windows-sdk-content
description: Retrieves the next entry in the Internet cache.
old-location: wininet\findnexturlcacheentry.htm
tech.root: wininet
ms.assetid: 776bf73e-00f3-46a1-a8c7-5eb365e9a518
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: FindNextUrlCacheEntry, FindNextUrlCacheEntry function [WinINet], FindNextUrlCacheEntryA, FindNextUrlCacheEntryW, _inet_findnexturlcacheentry_function, wininet.findnexturlcacheentry, wininet/FindNextUrlCacheEntry, wininet/FindNextUrlCacheEntryA, wininet/FindNextUrlCacheEntryW
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
req.unicode-ansi: FindNextUrlCacheEntryW (Unicode) and FindNextUrlCacheEntryA (ANSI)
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
 - FindNextUrlCacheEntry
 - FindNextUrlCacheEntryA
 - FindNextUrlCacheEntryW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FindNextUrlCacheEntryW function


## -description


Retrieves the next entry in the Internet cache.


## -parameters




### -param hEnumHandle [in]

Handle to the enumeration obtained from a previous call to 
<a href="https://msdn.microsoft.com/e8407284-846b-4080-b75b-4805330e0f95">FindFirstUrlCacheEntry</a>.


### -param lpNextCacheEntryInfo [out]

Pointer to an 
<a href="https://msdn.microsoft.com/7bda08e0-5df0-4087-a5cd-3a25c6ae5ade">INTERNET_CACHE_ENTRY_INFO</a> structure that receives information about the cache entry.


### -param lpcbCacheEntryInfo [in, out]

Pointer to a variable that specifies the size of the 
<i>lpNextCacheEntryInfo</i> buffer, in bytes. When the function returns, the variable contains the number of bytes copied to the buffer, or the size of the buffer required to retrieve the cache entry, in bytes.


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
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The size of 
<i>lpNextCacheEntryInfo</i> as specified by 
<i>lpdwNextCacheEntryInfoBufferSize</i> is not sufficient to contain all the information. The value returned in 
<i>lpdwNextCacheEntryInfoBufferSize</i> indicates the buffer size necessary to contain all the information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
The enumeration completed.

</td>
</tr>
</table>
 




## -remarks



Continue to call <b>FindNextUrlCacheEntry</b> until the last item in the cache is returned. 

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/44c268c9-a745-432a-8540-60d7e7d2cb2d">Caching</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

