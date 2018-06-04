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

# RetrieveUrlCacheEntryStreamA function


## -description


Provides the most efficient and implementation-independent way to access the cache data.


## -parameters




### -param lpszUrlName [in]

Pointer to a null-terminated string that contains the source name of the cache entry. This must be a unique name. The name string should not contain any escape characters.


### -param lpCacheEntryInfo [out]

Pointer to an 
<a href="https://msdn.microsoft.com/7bda08e0-5df0-4087-a5cd-3a25c6ae5ade">INTERNET_CACHE_ENTRY_INFO</a> structure that receives information about the cache entry.


### -param lpcbCacheEntryInfo [in, out]

Pointer to a variable that specifies the size, in bytes, of the 
<i>lpCacheEntryInfo</i> buffer. When the function returns, the variable receives the number of bytes copied to the buffer or the required size, in bytes, of the buffer. Note that this buffer size must accommodate both the <a href="https://msdn.microsoft.com/7bda08e0-5df0-4087-a5cd-3a25c6ae5ade">INTERNET_CACHE_ENTRY_INFO</a> structure and the associated strings that are stored immediately following it.


### -param fRandomRead [in]

Whether the stream is open for random access. Set the flag to <b>TRUE</b> to open the stream for random access.


### -param dwReserved [in]

This parameter is reserved and must be 0.


## -returns



If the function succeeds, the function returns a valid handle for use in the 
<a href="https://msdn.microsoft.com/8cfd0c64-25ca-4f08-b9b3-2743ded18030">ReadUrlCacheEntryStream</a> and 
<a href="https://msdn.microsoft.com/9fcc257e-732c-4545-a81b-7db20a98e497">UnlockUrlCacheEntryStream</a> functions.

If the function fails, it returns <b>NULL</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

Possible error values include the following.

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
The cache entry specified by the source name is not found in the cache storage.

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



<b>RetrieveUrlCacheEntryStream</b> does not do any URL parsing, so a URL containing an anchor (#) will not be found in the cache, even if the resource is cached. For example, if the URL http://adatum.com/example.htm#sample is passed, the function returns ERROR_FILE_NOT_FOUND even if http://adatum.com/example.htm is in the cache.

Cache clients that do not need URL data in the form of a file should use this function to access the data for a particular URL.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/44c268c9-a745-432a-8540-60d7e7d2cb2d">Caching</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

