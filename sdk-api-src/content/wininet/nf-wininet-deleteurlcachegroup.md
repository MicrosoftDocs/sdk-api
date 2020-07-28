---
UID: NF:wininet.DeleteUrlCacheGroup
title: DeleteUrlCacheGroup function (wininet.h)
description: Releases the specified GROUPID and any associated state in the cache index file.
helpviewer_keywords: ["DeleteUrlCacheGroup","DeleteUrlCacheGroup function [WinINet]","_inet_deleteurlcachegroup_function","wininet.deleteurlcachegroup","wininet/DeleteUrlCacheGroup"]
old-location: wininet\deleteurlcachegroup.htm
tech.root: wininet
ms.assetid: f1ff70db-36b7-4805-8f23-e3920acf0d11
ms.date: 12/05/2018
ms.keywords: DeleteUrlCacheGroup, DeleteUrlCacheGroup function [WinINet], _inet_deleteurlcachegroup_function, wininet.deleteurlcachegroup, wininet/DeleteUrlCacheGroup
f1_keywords:
- wininet/DeleteUrlCacheGroup
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DeleteUrlCacheGroup function


## -description


Releases the specified <b>GROUPID</b> and any associated state in the cache index file.


## -parameters




### -param GroupId [in]

ID of the cache group to be released.


### -param dwFlags [in]

Controls the cache group deletion. This can be set to 
any member of the <a href="https://docs.microsoft.com/windows/desktop/WinInet/cache-group-constants">cache group constants</a>. When this parameter is set to <a href="https://docs.microsoft.com/windows/desktop/WinInet/cache-group-constants">CACHEGROUP_FLAG_FLUSHURL_ONDELETE</a>, it causes 
<b>DeleteUrlCacheGroup</b> to delete all of the cache entries associated with this group, unless the entry belongs to another group.


### -param lpReserved [in]

This parameter is reserved and must be <b>NULL</b>.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get specific error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://docs.microsoft.com/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinInet/caching">Caching</a>



<a href="https://docs.microsoft.com/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
 

 

