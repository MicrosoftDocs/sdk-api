---
UID: NF:wininet.InternetInitializeAutoProxyDll
title: InternetInitializeAutoProxyDll function (wininet.h)
description: There are two WinINet functions named InternetInitializeAutoProxyDll.
helpviewer_keywords: ["InternetInitializeAutoProxyDll","InternetInitializeAutoProxyDll function [WinINet]","_inet_internetinitializeautoproxydll_function","wininet.internetinitializeautoproxydll","winineti/InternetInitializeAutoProxyDll"]
old-location: wininet\internetinitializeautoproxydll.htm
tech.root: wininet
ms.assetid: d55d64cb-ee92-4366-a1bb-f5d421ed81c8
ms.date: 12/05/2018
ms.keywords: InternetInitializeAutoProxyDll, InternetInitializeAutoProxyDll function [WinINet], _inet_internetinitializeautoproxydll_function, wininet.internetinitializeautoproxydll, winineti/InternetInitializeAutoProxyDll
f1_keywords:
- wininet/InternetInitializeAutoProxyDll
dev_langs:
- c++
req.header: wininet.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# InternetInitializeAutoProxyDll function

> [!Note]
> This function is deprecated. For autoproxy support, use HTTP Services (WinHTTP) version 5.1 instead. For more information, see [WinHTTP AutoProxy Support](https://docs.microsoft.com/windows/desktop/WinHttp/winhttp-autoproxy-support).


## -description

There are two WinINet functions named <b>InternetInitializeAutoProxyDll</b>. The first, which merely refreshes the internal state of proxy configuration information from the registry, has a single parameter as documented directly below.

The second function, prototyped as <b>pfnInternetInitializeAutoProxyDll</b>, is part of WinINet's limited autoproxy support, and must be called by dynamically linking to "JSProxy.dll".


## -parameters




### -param dwReserved [in]

This parameter is reserved and must be 0.


## -returns



Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



Because the <b>InternetInitializeAutoProxyDll</b> function takes time to complete its operation, it should not be called from  a UI thread.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://docs.microsoft.com/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wininet/nf-wininet-detectautoproxyurl">DetectAutoProxyUrl</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa384580(v=vs.85)">InternetDeInitializeAutoProxyDll</a>



<a href="https://docs.microsoft.com/windows/desktop/WinInet/internetgetproxyinfo">InternetGetProxyInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/WinHttp/winhttp-autoproxy-support">WinHTTP AutoProxy Support</a>
 

 

