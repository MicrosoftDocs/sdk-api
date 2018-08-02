---
UID: NS:wininet._INTERNET_CACHE_TIMESTAMPS
title: "_INTERNET_CACHE_TIMESTAMPS"
author: windows-sdk-content
description: Contains the LastModified and Expire times for a resource stored in the Internet cache.
old-location: wininet\internet_cache_timestamps.htm
old-project: WinInet
ms.assetid: e0fc2d73-95b9-4466-8a80-ca3211fc58e1
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "*LPINTERNET_CACHE_TIMESTAMPS, INTERNET_CACHE_TIMESTAMPS, INTERNET_CACHE_TIMESTAMPS structure [WinINet], LPINTERNET_CACHE_TIMESTAMPS, LPINTERNET_CACHE_TIMESTAMPS structure pointer [WinINet], _INTERNET_CACHE_TIMESTAMPS, _inet_internet_cache_timestamps_structure, wininet.internet_cache_timestamps, wininet/INTERNET_CACHE_TIMESTAMPS, wininet/LPINTERNET_CACHE_TIMESTAMPS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: INTERNET_CACHE_TIMESTAMPS, *LPINTERNET_CACHE_TIMESTAMPS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wininet.h
api_name:
 - INTERNET_CACHE_TIMESTAMPS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _INTERNET_CACHE_TIMESTAMPS structure


## -description


Contains the LastModified and Expire times for a resource stored in the Internet cache.


## -struct-fields




### -field ftExpires


<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that contains the Expires time. 


### -field ftLastModified


<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that contains the LastModified time. 


## -remarks



This structure is returned in the buffer when calling 
<a href="https://msdn.microsoft.com/b0bafd3d-8f54-429e-b423-dae3d61b0030">InternetQueryOption</a> with the 
<a href="https://msdn.microsoft.com/708510b8-468a-4287-849b-cba3d7001ea8">INTERNET_OPTION_CACHE_TIMESTAMPS</a> flag.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/b0bafd3d-8f54-429e-b423-dae3d61b0030">InternetQueryOption</a>
 

 

