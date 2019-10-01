---
UID: NF:wininet.CreateUrlCacheGroup
title: CreateUrlCacheGroup function (wininet.h)
author: windows-sdk-content
description: Generates cache group identifications.
old-location: wininet\createurlcachegroup.htm
tech.root: wininet
ms.assetid: bea0bc3b-75fb-4147-a4bd-f4290dfbf290
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateUrlCacheGroup, CreateUrlCacheGroup function [WinINet], _inet_createurlcachegroup_function, wininet.createurlcachegroup, wininet/CreateUrlCacheGroup
ms.topic: function
f1_keywords: 
 - "wininet/CreateUrlCacheGroup"
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
 - CreateUrlCacheGroup
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CreateUrlCacheGroup function


## -description


Generates cache group identifications.


## -parameters




### -param dwFlags [in]

Controls the creation of the cache group. This parameter can be set to 
<a href="https://docs.microsoft.com/windows/desktop/WinInet/cache-group-constants">CACHEGROUP_FLAG_GIDONLY</a>, which causes 
<b>CreateUrlCacheGroup</b> to generate a unique GROUPID, but does not create a physical group.


### -param lpReserved [in]

This parameter is reserved and must be <b>NULL</b>.


## -returns



Returns a valid <b>GROUPID</b> if successful, or <b>FALSE</b> otherwise. To get specific error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://docs.microsoft.com/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinInet/caching">Caching</a>



<a href="https://docs.microsoft.com/windows/desktop/WinInet/wininet-functions"> WinINet Functions</a>
 

 

