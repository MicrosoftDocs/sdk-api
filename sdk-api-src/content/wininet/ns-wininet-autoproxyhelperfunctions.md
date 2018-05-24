---
UID: NS:wininet.AutoProxyHelperFunctions
title: AutoProxyHelperFunctions
author: windows-driver-content
description: The AutoProxyHelperFunctions structure is used create a v-table of Proxy Auto-Config functions that can be passed to InternetInitializeAutoProxyDll.
old-location: wininet\autoproxyhelperfunctions.htm
old-project: WinInet
ms.assetid: 00574c2a-d72f-4744-82b7-3a980af59427
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: AutoProxyHelperFunctions, AutoProxyHelperFunctions structure [WinINet], wininet.autoproxyhelperfunctions, wininet/AutoProxyHelperFunctions
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: AutoProxyHelperFunctions
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wininet.h
api_name:
-	AutoProxyHelperFunctions
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# AutoProxyHelperFunctions structure


## -description


The <b>AutoProxyHelperFunctions</b> structure is used to create a v-table of Proxy Auto-Config (PAC) functions that can be passed to <a href="https://msdn.microsoft.com/d55d64cb-ee92-4366-a1bb-f5d421ed81c8">InternetInitializeAutoProxyDll</a>.

See the   <a href="Http://go.microsoft.com/fwlink/p/?linkid=84541">Navigator Proxy Auto-Config (PAC) File Format</a>  documentation for a specification of the form and use of Proxy Auto-Config helper functions.


## -struct-fields




### -field lpVtbl

Pointer to an <a href="https://msdn.microsoft.com/df482b8d-38e1-4d0d-a12c-8ba0f2e6423a">AutoProxyHelperVtbl</a> structure that contains an array of pointers to autoproxy helper functions. 


### -field AutoProxyHelperVtbl

 




## -remarks



Together with the <a href="https://msdn.microsoft.com/df482b8d-38e1-4d0d-a12c-8ba0f2e6423a">AutoProxyHelperVtbl</a> structure, <b>AutoProxyHelperFunctions</b> serves to create a standard v-table that can be declared and populated using C rather than requiring the use of C++.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/df482b8d-38e1-4d0d-a12c-8ba0f2e6423a">AutoProxyHelperVtbl</a>



<a href="https://msdn.microsoft.com/d55d64cb-ee92-4366-a1bb-f5d421ed81c8">InternetInitializeAutoProxyDll</a>
 

 

