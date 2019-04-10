---
UID: NF:wininet.FindNextUrlCacheGroup
title: FindNextUrlCacheGroup function (wininet.h)
author: windows-sdk-content
description: Retrieves the next cache group in a cache group enumeration started by FindFirstUrlCacheGroup.
old-location: wininet\findnexturlcachegroup.htm
tech.root: wininet
ms.assetid: f3cbe67c-c069-404c-8ca4-d18b35cc4c4a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FindNextUrlCacheGroup, FindNextUrlCacheGroup function [WinINet], _inet_findnexturlcachegroup_function, wininet.findnexturlcachegroup, wininet/FindNextUrlCacheGroup
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
 - FindNextUrlCacheGroup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FindNextUrlCacheGroup function


## -description


Retrieves the next cache group in a cache group enumeration started by 
<a href="https://msdn.microsoft.com/a333cbc6-a880-4b1c-be0d-abb083909638">FindFirstUrlCacheGroup</a>.


## -parameters




### -param hFind [in]

The cache group enumeration handle, which is returned by 
<a href="https://msdn.microsoft.com/a333cbc6-a880-4b1c-be0d-abb083909638">FindFirstUrlCacheGroup</a>.


### -param lpGroupId [out]

Pointer to a variable that receives the cache group identifier.


### -param lpReserved [in, out]

This parameter is reserved and must be <b>NULL</b>.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get specific error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Continue to call <b>FindNextUrlCacheGroup</b> until the last item in the cache is returned.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/44c268c9-a745-432a-8540-60d7e7d2cb2d">Caching</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97"> WinINet Functions</a>
 

 

