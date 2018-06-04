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

# SetUrlCacheEntryGroupA function


## -description


Adds entries to or removes entries from a cache group.


## -parameters




### -param lpszUrlName [in]

Pointer to a <b>null</b>-terminated string value that specifies the URL of the cached resource.


### -param dwFlags [in]

Determines whether the entry is added to or removed from a cache group. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_CACHE_GROUP_ADD</dt>
</dl>
</td>
<td width="60%">
Adds the cache entry to the cache group.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INTERNET_CACHE_GROUP_REMOVE</dt>
</dl>
</td>
<td width="60%">
Removes the entry from the cache group.

</td>
</tr>
</table>
 


### -param GroupId [in]

Identifier of the cache group that the entry will be added to or removed from.


### -param pbGroupAttributes [in]

This parameter is reserved and must be <b>NULL</b>.


### -param cbGroupAttributes [in]

This parameter is reserved and must be 0.


### -param lpReserved [in]

This parameter is reserved and must be <b>NULL</b>.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.




## -remarks



A cache entry can belong to more than one cache group.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/44c268c9-a745-432a-8540-60d7e7d2cb2d">Caching</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

