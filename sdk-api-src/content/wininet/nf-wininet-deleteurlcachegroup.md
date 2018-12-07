---
UID: NF:wininet.DeleteUrlCacheGroup
title: DeleteUrlCacheGroup function
author: windows-sdk-content
description: Releases the specified GROUPID and any associated state in the cache index file.
old-location: wininet\deleteurlcachegroup.htm
tech.root: wininet
ms.assetid: f1ff70db-36b7-4805-8f23-e3920acf0d11
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DeleteUrlCacheGroup, DeleteUrlCacheGroup function [WinINet], _inet_deleteurlcachegroup_function, wininet.deleteurlcachegroup, wininet/DeleteUrlCacheGroup
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
req.unicode-ansi: 
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
 - DeleteUrlCacheGroup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DeleteUrlCacheGroup function


## -description


Releases the specified <b>GROUPID</b> and any associated state in the cache index file.


## -parameters




### -param GroupId [in]

ID of the cache group to be released.


### -param dwFlags [in]

Controls the cache group deletion. This can be set to 
any member of the <a href="https://msdn.microsoft.com/9ca2069e-497d-4747-acf4-d5b8020b8ab7">cache group constants</a>. When this parameter is set to <a href="https://msdn.microsoft.com/en-us/library/Aa383923(v=VS.85).aspx">CACHEGROUP_FLAG_FLUSHURL_ONDELETE</a>, it causes 
<b>DeleteUrlCacheGroup</b> to delete all of the cache entries associated with this group, unless the entry belongs to another group.


### -param lpReserved [in]

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
 

 

