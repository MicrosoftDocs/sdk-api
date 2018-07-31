---
UID: NF:wininet.GetUrlCacheGroupAttributeW
title: GetUrlCacheGroupAttributeW function
author: windows-sdk-content
description: Retrieves the attribute information of the specified cache group.
old-location: wininet\geturlcachegroupattribute.htm
old-project: WinInet
ms.assetid: 5e4e5666-1999-4bea-9b3e-f435f5dcfff8
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetUrlCacheGroupAttribute, GetUrlCacheGroupAttribute function [WinINet], GetUrlCacheGroupAttributeA, GetUrlCacheGroupAttributeW, _inet_geturlcachegroupattribute_function, wininet.geturlcachegroupattribute, wininet/GetUrlCacheGroupAttribute, wininet/GetUrlCacheGroupAttributeA, wininet/GetUrlCacheGroupAttributeW
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
req.unicode-ansi: GetUrlCacheGroupAttributeW (Unicode) and GetUrlCacheGroupAttributeA (ANSI)
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
 - GetUrlCacheGroupAttribute
 - GetUrlCacheGroupAttributeA
 - GetUrlCacheGroupAttributeW
product: Windows
targetos: Windows
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetUrlCacheGroupAttributeW function


## -description


Retrieves the attribute information of the specified cache group.


## -parameters




### -param gid [in]

Identifier of the cache group.


### -param dwFlags [in]

This parameter is reserved and must be 0.


### -param dwAttributes [in]

Attributes to be retrieved. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>CACHEGROUP_ATTRIBUTE_BASIC</dt>
</dl>
</td>
<td width="60%">
Retrieves the flags, type, and disk quota attributes of the cache group.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>CACHEGROUP_ATTRIBUTE_FLAG</dt>
</dl>
</td>
<td width="60%">
Sets or retrieves the flags associated with the cache group.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>CACHEGROUP_ATTRIBUTE_GET_ALL</dt>
</dl>
</td>
<td width="60%">
Retrieves all the attributes of the cache group.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>CACHEGROUP_ATTRIBUTE_GROUPNAME</dt>
</dl>
</td>
<td width="60%">
Sets or retrieves the group name of the cache group.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>CACHEGROUP_ATTRIBUTE_QUOTA</dt>
</dl>
</td>
<td width="60%">
Sets or retrieves the disk quota associated with the cache group.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>CACHEGROUP_ATTRIBUTE_STORAGE</dt>
</dl>
</td>
<td width="60%">
Sets or retrieves the group owner storage associated with the cache group.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>CACHEGROUP_ATTRIBUTE_TYPE</dt>
</dl>
</td>
<td width="60%">
Sets or retrieves the cache group type.

</td>
</tr>
</table>
 


### -param lpGroupInfo [out]

Pointer to an 
<a href="https://msdn.microsoft.com/d1c30fee-b8a3-472d-91a5-9d081f66b007">INTERNET_CACHE_GROUP_INFO</a> structure that receives the requested information.


### -param lpcbGroupInfo

TBD


### -param lpReserved [in, out]

This parameter is reserved and must be <b>NULL</b>.


#### - lpdwGroupInfo [in, out]

Pointer to a variable that contains the size of the 
<i>lpGroupInfo</i> buffer. When the function returns, the variable contains the number of bytes copied to the buffer, or the required size of the buffer, in bytes.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get specific error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/44c268c9-a745-432a-8540-60d7e7d2cb2d">Caching</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97"> WinINet Functions</a>
 

 

