---
UID: NF:wininet.HttpEndRequestW
title: HttpEndRequestW function
author: windows-driver-content
description: Ends an HTTP request that was initiated by HttpSendRequestEx.
old-location: wininet\httpendrequest.htm
old-project: WinInet
ms.assetid: 6ea91da6-0bc2-49b6-a56b-c4224ad73b81
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: HttpEndRequest, HttpEndRequest function [WinINet], HttpEndRequestA, HttpEndRequestW, _win32_httpendrequest, wininet.httpendrequest, wininet/HttpEndRequest, wininet/HttpEndRequestA, wininet/HttpEndRequestW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: HttpEndRequestW (Unicode) and HttpEndRequestA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: InternetCookieState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wininet.dll
api_name:
-	HttpEndRequest
-	HttpEndRequestA
-	HttpEndRequestW
product: Windows
targetos: Windows
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# HttpEndRequestW function


## -description


Ends an HTTP request that was initiated by 
<a href="https://msdn.microsoft.com/3362fcd2-e8df-4886-9525-bf60589b2c1f">HttpSendRequestEx</a>.


## -parameters




### -param hRequest [in]


						Handle returned by 
<a href="https://msdn.microsoft.com/caaff8e8-7db9-4d6d-8ba2-d8d19475173a">HttpOpenRequest</a> and sent by 
<a href="https://msdn.microsoft.com/3362fcd2-e8df-4886-9525-bf60589b2c1f">HttpSendRequestEx</a>.


### -param lpBuffersOut [out, optional]

This parameter is reserved and must be <b>NULL</b>.


### -param dwFlags [in]

This parameter is reserved and must be set to 0.


### -param dwContext [in, optional]

This parameter is reserved and must be set to 0.


## -returns



If the function succeeds, the function returns <b>TRUE</b>.


If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If 
<i>lpBuffersOut</i> is not set to <b>NULL</b>, 
<b>HttpEndRequest</b> will return ERROR_INVALID_PARAMETER.
			

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/0f307e28-9c38-41e7-9795-7eef08e99a3c">HTTP Sessions</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

