---
UID: NF:wininet.FindCloseUrlCache
title: FindCloseUrlCache function
author: windows-sdk-content
description: Closes the specified cache enumeration handle.
old-location: wininet\findcloseurlcache.htm
old-project: WinInet
ms.assetid: 54fc7bea-4cc1-4034-93c3-49ec88817648
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: FindCloseUrlCache, FindCloseUrlCache function [WinINet], _inet_findcloseurlcache_function, wininet.findcloseurlcache, wininet/FindCloseUrlCache
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
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: InternetCookieState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wininet.dll
api_name:
-	FindCloseUrlCache
product: Windows
targetos: Windows
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# FindCloseUrlCache function


## -description


Closes the specified cache enumeration handle.


## -parameters




### -param hEnumHandle [in]

Handle returned by a previous call to the 
<a href="https://msdn.microsoft.com/e8407284-846b-4080-b75b-4805330e0f95">FindFirstUrlCacheEntry</a> function.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/44c268c9-a745-432a-8540-60d7e7d2cb2d">Caching</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

