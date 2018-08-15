---
UID: NF:winineti.FreeUrlCacheSpaceA
title: FreeUrlCacheSpaceA function
author: windows-sdk-content
description: Frees space in the cache.
old-location: wininet\freeurlcachespace.htm
old-project: wininet
ms.assetid: 5853CA64-551F-484E-A992-25B9EA6C74C2
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: FreeUrlCacheSpace, FreeUrlCacheSpace function [WinINet], FreeUrlCacheSpaceA, FreeUrlCacheSpaceW, wininet.freeurlcachespace, winineti/FreeUrlCacheSpace, winineti/FreeUrlCacheSpaceA, winineti/FreeUrlCacheSpaceW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winineti.h
req.include-header: 
req.redist: 
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
req.typenames: INTERNET_AUTH_NOTIFY_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wininet.dll
api_name:
 - FreeUrlCacheSpace
 - FreeUrlCacheSpaceA
 - FreeUrlCacheSpaceW
product: Windows
targetos: Windows
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# FreeUrlCacheSpaceA function


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Frees space in the cache.<div class="alert"><b>Note</b>  This API is deprecated. Please use the <a href="https://msdn.microsoft.com/library/windows/desktop/gg269259">Extensible Storage Engine</a> instead.</div>
<div> </div>



## -parameters




### -param lpszCachePath

The path for the cache.


### -param dwSize

The percentage of the cache to free (in the range 1 to 100, inclusive).


### -param dwFilter [in]

This parameter is reserved, and must be 0.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service nor when impersonating a security context. For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/44c268c9-a745-432a-8540-60d7e7d2cb2d">Caching</a>



<a href="https://msdn.microsoft.com/library/windows/desktop/mt814933">CreateUrlCacheContainer</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

