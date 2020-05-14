---
UID: NF:winineti.DeleteUrlCacheContainerA
title: DeleteUrlCacheContainerA function (winineti.h)
description: Deletes a cache container (which contains cache entries) based on the specified name.helpviewer_keywords: ["DeleteUrlCacheContainer","DeleteUrlCacheContainer function [WinINet]","DeleteUrlCacheContainerA","DeleteUrlCacheContainerW","wininet.deleteurlcachecontainer","winineti/DeleteUrlCacheContainer","winineti/DeleteUrlCacheContainerA","winineti/DeleteUrlCacheContainerW"]
old-location: wininet\deleteurlcachecontainer.htm
tech.root: wininet
ms.assetid: 97F46974-9B20-46C6-B742-4BA5C60491DA
ms.date: 12/05/2018
ms.keywords: DeleteUrlCacheContainer, DeleteUrlCacheContainer function [WinINet], DeleteUrlCacheContainerA, DeleteUrlCacheContainerW, wininet.deleteurlcachecontainer, winineti/DeleteUrlCacheContainer, winineti/DeleteUrlCacheContainerA, winineti/DeleteUrlCacheContainerW
f1_keywords:
- winineti/DeleteUrlCacheContainer
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DeleteUrlCacheContainerA function


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Deletes a cache container (which contains cache entries) based on the specified name.<div class="alert"><b>Note</b>  This API is deprecated. Please use the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/Gg269259(v=EXCHG.10)">Extensible Storage Engine</a> instead.</div>
<div> </div>



## -parameters




### -param Name

The name of the cache container to be deleted.


### -param dwOptions

This parameter is reserved, and must be 0.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service nor when impersonating a security context. For server implementations or services use <a href="https://docs.microsoft.com/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinInet/caching">Caching</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winineti/nf-winineti-createurlcachecontainera">CreateUrlCacheContainer</a>



<a href="https://docs.microsoft.com/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
 

 

