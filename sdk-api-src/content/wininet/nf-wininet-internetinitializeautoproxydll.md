---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# InternetInitializeAutoProxyDll function


## -description


There are two WinINet functions named <b>InternetInitializeAutoProxyDll</b>. The first, which merely refreshes the internal state of proxy configuration information from the registry, has a single parameter as documented directly below. 

The second function, prototyped as <b>pfnInternetInitializeAutoProxyDll</b>, is part of WinINet's limited autoproxy support, and must be called by dynamically linking to "JSProxy.dll". For autoproxy support, use Windows HTTP Services (WinHTTP) version 5.1. For more information, see <a href="http.using_the_winhttp_autoproxy_feature">WinHTTP AutoProxy Support</a>.


## -parameters




### -param dwReserved [in]

This parameter is reserved and must be 0.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Because the <b>InternetInitializeAutoProxyDll</b> function takes time to complete its operation, it should not be called from  a UI thread.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/4e94ab0c-0f39-4e6e-a272-6beff61e97c6">DetectAutoProxyUrl</a>



<a href="https://msdn.microsoft.com/ccb69e89-9407-48ac-bb70-fbc425bd1051">InternetDeInitializeAutoProxyDll</a>



<a href="https://msdn.microsoft.com/5fc0f471-420c-4125-8323-cb1e1e72e43f">InternetGetProxyInfo</a>



<a href="http.using_the_winhttp_autoproxy_feature">WinHTTP AutoProxy Support</a>
 

 

