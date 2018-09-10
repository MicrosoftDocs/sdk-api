---
UID: NF:winineti.DeleteUrlCacheContainerW
title: DeleteUrlCacheContainerW function
author: windows-sdk-content
description: Deletes a cache container (which contains cache entries) based on the specified name.
old-location: wininet\deleteurlcachecontainer.htm
tech.root: WinInet
ms.assetid: 97F46974-9B20-46C6-B742-4BA5C60491DA
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: DeleteUrlCacheContainer, DeleteUrlCacheContainer function [WinINet], DeleteUrlCacheContainerA, DeleteUrlCacheContainerW, wininet.deleteurlcachecontainer, winineti/DeleteUrlCacheContainer, winineti/DeleteUrlCacheContainerA, winineti/DeleteUrlCacheContainerW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winineti.h
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
 - DeleteUrlCacheContainer
 - DeleteUrlCacheContainerA
 - DeleteUrlCacheContainerW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DeleteUrlCacheContainerW function


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Deletes a cache container (which contains cache entries) based on the specified name.<div class="alert"><b>Note</b>  This API is deprecated. Please use the <a href="https://msdn.microsoft.com/library/windows/desktop/gg269259">Extensible Storage Engine</a> instead.</div>
<div> </div>



## -parameters




### -param Name

The name of the cache container to be deleted.


### -param dwOptions

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
 

 

