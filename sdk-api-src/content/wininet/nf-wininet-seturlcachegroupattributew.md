---
UID: NF:wininet.SetUrlCacheGroupAttributeW
title: SetUrlCacheGroupAttributeW function (wininet.h)
author: windows-sdk-content
description: Sets the attribute information of the specified cache group.
old-location: wininet\seturlcachegroupattribute.htm
tech.root: wininet
ms.assetid: dd4e94cd-0fe5-414a-8a43-8777403e8a45
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SetUrlCacheGroupAttribute, SetUrlCacheGroupAttribute function [WinINet], SetUrlCacheGroupAttributeA, SetUrlCacheGroupAttributeW, _inet_seturlcachegroupattribute_function, wininet.seturlcachegroupattribute, wininet/SetUrlCacheGroupAttribute, wininet/SetUrlCacheGroupAttributeA, wininet/SetUrlCacheGroupAttributeW
ms.topic: function
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetUrlCacheGroupAttributeW (Unicode) and SetUrlCacheGroupAttributeA (ANSI)
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
 - SetUrlCacheGroupAttribute
 - SetUrlCacheGroupAttributeA
 - SetUrlCacheGroupAttributeW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetUrlCacheGroupAttributeW function


## -description


Sets the attribute information of the specified cache group.


## -parameters




### -param gid [in]

Identifier of the cache group.


### -param dwFlags [in]

This parameter is reserved and must be 0.


### -param dwAttributes [in]

Attributes to be set. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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
<tr>
<td width="40%">
<dl>
<dt>CACHEGROUP_READWRITE_MASK</dt>
</dl>
</td>
<td width="60%">
Sets the type, disk quota, group name, and owner storage attributes of the cache group.

</td>
</tr>
</table>
 


### -param lpGroupInfo [in]

Pointer to an 
<a href="https://msdn.microsoft.com/d1c30fee-b8a3-472d-91a5-9d081f66b007">INTERNET_CACHE_GROUP_INFO</a> structure that specifies the attribute information to be stored.


### -param lpReserved [in, out]

This parameter is reserved and must be <b>NULL</b>.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get specific error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/44c268c9-a745-432a-8540-60d7e7d2cb2d">Caching</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

