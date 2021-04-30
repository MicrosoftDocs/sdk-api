---
UID: NS:wininet.AutoProxyHelperFunctions
title: AutoProxyHelperFunctions (wininet.h)
description: The AutoProxyHelperFunctions structure is used create a v-table of Proxy Auto-Config functions that can be passed to InternetInitializeAutoProxyDll.
helpviewer_keywords: ["AutoProxyHelperFunctions","AutoProxyHelperFunctions structure [WinINet]","wininet.autoproxyhelperfunctions","wininet/AutoProxyHelperFunctions"]
old-location: wininet\autoproxyhelperfunctions.htm
tech.root: wininet
ms.assetid: 00574c2a-d72f-4744-82b7-3a980af59427
ms.date: 12/05/2018
ms.keywords: AutoProxyHelperFunctions, AutoProxyHelperFunctions structure [WinINet], wininet.autoproxyhelperfunctions, wininet/AutoProxyHelperFunctions
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: AutoProxyHelperFunctions
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AutoProxyHelperFunctions
 - wininet/AutoProxyHelperFunctions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wininet.h
api_name:
 - AutoProxyHelperFunctions
---

# AutoProxyHelperFunctions structure


## -description

The <b>AutoProxyHelperFunctions</b> structure is used to create a v-table of Proxy Auto-Config (PAC) functions that can be passed to <a href="/windows/desktop/api/wininet/nf-wininet-internetinitializeautoproxydll">InternetInitializeAutoProxyDll</a>.

See the   <a href="https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html">Navigator Proxy Auto-Config (PAC) File Format</a>  documentation for a specification of the form and use of Proxy Auto-Config helper functions.

## -struct-fields

### -field lpVtbl

Pointer to an <a href="/windows/desktop/api/wininet/ns-wininet-autoproxyhelpervtbl">AutoProxyHelperVtbl</a> structure that contains an array of pointers to autoproxy helper functions.

### -field AutoProxyHelperVtbl

## -remarks

Together with the <a href="/windows/desktop/api/wininet/ns-wininet-autoproxyhelpervtbl">AutoProxyHelperVtbl</a> structure, <b>AutoProxyHelperFunctions</b> serves to create a standard v-table that can be declared and populated using C rather than requiring the use of C++.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wininet/ns-wininet-autoproxyhelpervtbl">AutoProxyHelperVtbl</a>



<a href="/windows/desktop/api/wininet/nf-wininet-internetinitializeautoproxydll">InternetInitializeAutoProxyDll</a>