---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# FindNextUrlCacheEntryExA function


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
 

 

