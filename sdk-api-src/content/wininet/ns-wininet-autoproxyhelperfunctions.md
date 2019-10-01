---
UID: NS:wininet.AutoProxyHelperFunctions
title: AutoProxyHelperFunctions (wininet.h)
author: windows-sdk-content
description: The AutoProxyHelperFunctions structure is used create a v-table of Proxy Auto-Config functions that can be passed to InternetInitializeAutoProxyDll.
old-location: wininet\autoproxyhelperfunctions.htm
tech.root: wininet
ms.assetid: 00574c2a-d72f-4744-82b7-3a980af59427
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AutoProxyHelperFunctions, AutoProxyHelperFunctions structure [WinINet], wininet.autoproxyhelperfunctions, wininet/AutoProxyHelperFunctions
ms.topic: struct
f1_keywords: 
 - "wininet/AutoProxyHelperFunctions"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wininet.h
api_name:
 - AutoProxyHelperFunctions
targetos: Windows
req.typenames: AutoProxyHelperFunctions
req.redist: 
ms.custom: 19H1
---

# AutoProxyHelperFunctions structure


## -description


The <b>AutoProxyHelperFunctions</b> structure is used to create a v-table of Proxy Auto-Config (PAC) functions that can be passed to <a href="https://docs.microsoft.com/windows/desktop/api/wininet/nf-wininet-internetinitializeautoproxydll">InternetInitializeAutoProxyDll</a>.

See the   <a href="Http://go.microsoft.com/fwlink/p/?linkid=84541">Navigator Proxy Auto-Config (PAC) File Format</a>  documentation for a specification of the form and use of Proxy Auto-Config helper functions.


## -struct-fields




### -field lpVtbl

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/wininet/ns-wininet-autoproxyhelpervtbl">AutoProxyHelperVtbl</a> structure that contains an array of pointers to autoproxy helper functions. 


### -field AutoProxyHelperVtbl

 




## -remarks



Together with the <a href="https://docs.microsoft.com/windows/desktop/api/wininet/ns-wininet-autoproxyhelpervtbl">AutoProxyHelperVtbl</a> structure, <b>AutoProxyHelperFunctions</b> serves to create a standard v-table that can be declared and populated using C rather than requiring the use of C++.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://docs.microsoft.com/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wininet/ns-wininet-autoproxyhelpervtbl">AutoProxyHelperVtbl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wininet/nf-wininet-internetinitializeautoproxydll">InternetInitializeAutoProxyDll</a>
 

 

