---
UID: NF:winineti.InternetInitializeAutoProxyDll
title: InternetInitializeAutoProxyDll function (winineti.h)
description: There are two WinINet functions named InternetInitializeAutoProxyDll. The first refreshes the internal state of proxy configuration and the second is part of WinINet's autoproxy support.
helpviewer_keywords: ["InternetInitializeAutoProxyDll","InternetInitializeAutoProxyDll function [WinINet]","_inet_internetinitializeautoproxydll_function","wininet.internetinitializeautoproxydll","winineti/InternetInitializeAutoProxyDll"]
old-location: wininet\internetinitializeautoproxydll.htm
tech.root: wininet
ms.assetid: d55d64cb-ee92-4366-a1bb-f5d421ed81c8
ms.date: 08/15/2022
ms.keywords: InternetInitializeAutoProxyDll, InternetInitializeAutoProxyDll function [WinINet], _inet_internetinitializeautoproxydll_function, wininet.internetinitializeautoproxydll, winineti/InternetInitializeAutoProxyDll
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
req.lib: wininet.Lib
req.dll: JSProxy.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InternetInitializeAutoProxyDll
 - winineti/InternetInitializeAutoProxyDll
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - JSProxy.dll
api_name:
 - InternetInitializeAutoProxyDll
---

# InternetInitializeAutoProxyDll function


## -description

There are two WinINet functions named <b>InternetInitializeAutoProxyDll</b>. The first, which merely refreshes the internal state of proxy configuration information from the registry, has a single parameter as documented directly below. 

The second function, prototyped as <b>pfnInternetInitializeAutoProxyDll</b>, is part of WinINet's limited autoproxy support, and must be called by dynamically linking to "JSProxy.dll". For autoproxy support, use Windows HTTP Services (WinHTTP) version 5.1. For more information, see <a href="/windows/desktop/WinHttp/winhttp-autoproxy-support">WinHTTP AutoProxy Support</a>.

## -parameters

### -param dwReserved [in]

This parameter is reserved and must be 0.

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Because the <b>InternetInitializeAutoProxyDll</b> function takes time to complete its operation, it should not be called from  a UI thread.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wininet/nf-wininet-detectautoproxyurl">DetectAutoProxyUrl</a>



<a href="/previous-versions/windows/desktop/legacy/aa384580(v=vs.85)">InternetDeInitializeAutoProxyDll</a>



<a href="/windows/desktop/WinInet/internetgetproxyinfo">InternetGetProxyInfo</a>



<a href="/windows/desktop/WinHttp/winhttp-autoproxy-support">WinHTTP AutoProxy Support</a>
