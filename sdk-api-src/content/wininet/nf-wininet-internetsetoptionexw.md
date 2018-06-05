---
UID: NF:wininet.InternetSetOptionExW
title: InternetSetOptionExW function
author: windows-sdk-content
description: Not supported.Implemented only as a stub that calls the InternetSetOption function; InternetSetOptionEx has no functionality of its own. Do not use this function at this time.
old-location: wininet\internetsetoptionex.htm
old-project: WinInet
ms.assetid: 535e4f38-d941-4b69-8c48-ea47f3fbd5e7
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: InternetSetOptionEx, InternetSetOptionEx function [WinINet], InternetSetOptionExA, InternetSetOptionExW, _inet_internetsetoptionex_function, wininet.internetsetoptionex, wininet/InternetSetOptionEx, wininet/InternetSetOptionExA, wininet/InternetSetOptionExW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: InternetSetOptionExW (Unicode) and InternetSetOptionExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: InternetCookieState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wininet.dll
api_name:
-	InternetSetOptionEx
-	InternetSetOptionExA
-	InternetSetOptionExW
product: Windows
targetos: Windows
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# InternetSetOptionExW function


## -description


Not supported.

Implemented only as a stub that calls the <a href="https://msdn.microsoft.com/578c7130-7426-4a2e-ae0f-ed8a84449b06">InternetSetOption</a> function; <b>InternetSetOptionEx</b> has no functionality of its own. Do not use this function at this time.


## -parameters




### -param hInternet

TBD


### -param dwOption

TBD


### -param lpBuffer

TBD


### -param dwBufferLength

TBD


### -param dwFlags

TBD




## -returns



This function does not return a value.




## -remarks



<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/578c7130-7426-4a2e-ae0f-ed8a84449b06">InternetSetOption</a>
 

 

