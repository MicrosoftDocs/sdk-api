---
UID: NF:winineti.InternetInitializeAutoProxyDll
title: InternetInitializeAutoProxyDll function
author: windows-sdk-content
description: There are two WinINet functions named InternetInitializeAutoProxyDll.
old-location: wininet\internetinitializeautoproxydll.htm
tech.root: wininet
ms.assetid: d55d64cb-ee92-4366-a1bb-f5d421ed81c8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: InternetInitializeAutoProxyDll, InternetInitializeAutoProxyDll function [WinINet], _inet_internetinitializeautoproxydll_function, wininet.internetinitializeautoproxydll, winineti/InternetInitializeAutoProxyDll
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winineti.h
req.include-header: Wininet.h
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
req.lib: 
req.dll: JSProxy.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - JSProxy.dll
api_name:
 - InternetInitializeAutoProxyDll
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# InternetInitializeAutoProxyDll function


## -description


There are two WinINet functions named <b>InternetInitializeAutoProxyDll</b>. The first, which merely refreshes the internal state of proxy configuration information from the registry, has a single parameter as documented directly below. 

The second function, prototyped as <b>pfnInternetInitializeAutoProxyDll</b>, is part of WinINet's limited autoproxy support, and must be called by dynamically linking to "JSProxy.dll". For autoproxy support, use Windows HTTP Services (WinHTTP) version 5.1. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Aa384240(v=VS.85).aspx">WinHTTP AutoProxy Support</a>.


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



<a href="https://msdn.microsoft.com/en-us/library/Aa384240(v=VS.85).aspx">WinHTTP AutoProxy Support</a>
 

 

