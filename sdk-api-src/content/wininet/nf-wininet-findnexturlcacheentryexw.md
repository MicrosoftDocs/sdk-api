---
UID: NF:wininet.FindNextUrlCacheEntryExW
title: FindNextUrlCacheEntryExW function
author: windows-driver-content
description: Finds the next cache entry in a cache enumeration started by the FindFirstUrlCacheEntryEx function.
old-location: wininet\findnexturlcacheentryex.htm
old-project: WinInet
ms.assetid: 39484e35-cd25-4e48-ace0-16033d3e6954
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: FindNextUrlCacheEntryEx, FindNextUrlCacheEntryEx function [WinINet], FindNextUrlCacheEntryExA, FindNextUrlCacheEntryExW, _inet_findnexturlcacheentryex_function, wininet.findnexturlcacheentryex, wininet/FindNextUrlCacheEntryEx, wininet/FindNextUrlCacheEntryExA, wininet/FindNextUrlCacheEntryExW
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
req.unicode-ansi: FindNextUrlCacheEntryExW (Unicode) and FindNextUrlCacheEntryExA (ANSI)
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
-	FindNextUrlCacheEntryEx
-	FindNextUrlCacheEntryExA
-	FindNextUrlCacheEntryExW
product: Windows
targetos: Windows
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# FindNextUrlCacheEntryExW function


## -description


Finds the next cache entry in a cache enumeration started by the 
<a href="https://msdn.microsoft.com/af17c809-2a9e-443a-b64a-93c028e3b71b">FindFirstUrlCacheEntryEx</a> function.


## -parameters




### -param hEnumHandle [in]

Handle returned by 
<a href="https://msdn.microsoft.com/af17c809-2a9e-443a-b64a-93c028e3b71b">FindFirstUrlCacheEntryEx</a>, which started a cache enumeration.


### -param lpNextCacheEntryInfo [in, out]

Pointer to the  
<a href="https://msdn.microsoft.com/7bda08e0-5df0-4087-a5cd-3a25c6ae5ade">INTERNET_CACHE_ENTRY_INFO</a> structure that receives the cache entry information.


### -param lpcbCacheEntryInfo

TBD


### -param lpGroupAttributes

This parameter is reserved and must be <b>NULL</b>.


### -param lpcbGroupAttributes

This parameter is reserved and must be <b>NULL</b>.


### -param lpReserved

This parameter is reserved.


#### - lpcbEntryInfo [in, out]

Pointer to a variable that indicates the size of the buffer, in bytes.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get specific error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Continue to call <b>FindNextUrlCacheEntryEx</b> until the last item in the cache is returned.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/44c268c9-a745-432a-8540-60d7e7d2cb2d">Caching</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

