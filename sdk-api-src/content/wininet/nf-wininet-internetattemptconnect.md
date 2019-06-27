---
UID: NF:wininet.InternetAttemptConnect
title: InternetAttemptConnect function (wininet.h)
author: windows-sdk-content
description: Attempts to make a connection to the Internet.
old-location: wininet\internetattemptconnect.htm
tech.root: wininet
ms.assetid: a6f22704-f7ca-4c4d-91c3-304b592db6ca
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: InternetAttemptConnect, InternetAttemptConnect function [WinINet], _inet_internetattemptconnect_function, wininet.internetattemptconnect, wininet/InternetAttemptConnect
ms.topic: function
f1_keywords: 
 - "wininet/InternetAttemptConnect"
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
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wininet.dll
api_name:
 - InternetAttemptConnect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# InternetAttemptConnect function


## -description


Attempts to make a connection to the Internet.


## -parameters




### -param dwReserved [in]

This parameter is reserved and must be 0.


## -returns



Returns ERROR_SUCCESS if successful, or a <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error code</a> otherwise.




## -remarks



This function allows an application to first attempt to connect before issuing any requests. A client program can use this to evoke the dial-up dialog box. If the attempt fails, the application should enter offline mode.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://docs.microsoft.com/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinInet/enabling-internet-functionality">Enabling Internet Functionality</a>



<a href="https://docs.microsoft.com/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
 

 

