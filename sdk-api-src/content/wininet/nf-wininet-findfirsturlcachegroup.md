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

# FindFirstUrlCacheGroup function


## -description


Initiates the enumeration of the cache groups in the Internet cache.


## -parameters




### -param dwFlags [in]

This parameter is reserved and must be 0.


### -param dwFilter [in]

Filters to be used. This parameter can be zero or one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>CACHEGROUP_SEARCH_ALL</dt>
</dl>
</td>
<td width="60%">
Search all  cache groups.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>CACHEGROUP_SEARCH_BYURL</dt>
</dl>
</td>
<td width="60%">
Not currently implemented.

</td>
</tr>
</table>
 


### -param lpSearchCondition [in]

This parameter is reserved and must be <b>NULL</b>.


### -param dwSearchCondition [in]

This parameter is reserved and must be 0.


### -param lpGroupId [out]

Pointer to the ID of the first cache group that matches the search criteria.


### -param lpReserved [in, out]

This parameter is reserved and must be <b>NULL</b>.


## -returns



Returns a valid handle to the first item in the enumeration if successful, or <b>NULL</b> otherwise. To get specific error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. If the function finds no matching files, 
<b>GetLastError</b> returns ERROR_NO_MORE_FILES.




## -remarks



The handle returned from <b>FindFirstUrlCacheGroup</b> is used in subsequent calls to <a href="https://msdn.microsoft.com/f3cbe67c-c069-404c-8ca4-d18b35cc4c4a">FindNextUrlCacheGroup</a>. At the end of the enumeration, the application should call 
<a href="https://msdn.microsoft.com/54fc7bea-4cc1-4034-93c3-49ec88817648">FindCloseUrlCache</a>.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/44c268c9-a745-432a-8540-60d7e7d2cb2d">Caching</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97"> WinINet Functions</a>
 

 

