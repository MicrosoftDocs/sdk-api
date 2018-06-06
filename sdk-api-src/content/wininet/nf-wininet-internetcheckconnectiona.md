---
UID: NF:wininet.InternetCheckConnectionA
title: InternetCheckConnectionA function
author: windows-sdk-content
description: Allows an application to check if a connection to the Internet can be established.
old-location: wininet\internetcheckconnection.htm
old-project: WinInet
ms.assetid: 4666e4ee-057e-452d-ac2c-d03321a0073f
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: InternetCheckConnection, InternetCheckConnection function [WinINet], InternetCheckConnectionA, InternetCheckConnectionW, _inet_internetcheckconnection_function, wininet.internetcheckconnection, wininet/InternetCheckConnection, wininet/InternetCheckConnectionA, wininet/InternetCheckConnectionW
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
req.unicode-ansi: InternetCheckConnectionW (Unicode) and InternetCheckConnectionA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: InternetCookieState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wininet.dll
api_name:
 - InternetCheckConnection
 - InternetCheckConnectionA
 - InternetCheckConnectionW
product: Windows
targetos: Windows
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# InternetCheckConnectionA function


## -description


<p class="CCE_Message">[<b>InternetCheckConnection</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://go.microsoft.com/fwlink/p/?linkid=861634">NetworkInformation.GetInternetConnectionProfile</a> or the <a href="https://msdn.microsoft.com/57cc2a07-4551-428c-a303-9b1a4510f225">NLM Interfaces</a>.
]

Allows an application to check if a connection to the Internet can be established.


## -parameters




### -param lpszUrl [in]

Pointer to a <b>null</b>-terminated string that specifies the URL to use to check the connection. This value can be <b>NULL</b>.


### -param dwFlags [in]

Options. FLAG_ICC_FORCE_CONNECTION is the only flag that is currently available. If this flag is set, it forces a connection. A sockets connection is attempted in the following order:

<ul>
<li>If 
<i>lpszUrl</i> is non-<b>NULL</b>, the host value is extracted from it and used to ping that specific host.</li>
<li>If 
<i>lpszUrl</i> is <b>NULL</b> and there is an entry in the internal server database for the nearest server, the host value is extracted from the entry and used to ping that server.</li>
</ul>

### -param dwReserved [in]

This parameter is reserved and must be 0.


## -returns



Returns <b>TRUE</b> if a connection is made successfully, or <b>FALSE</b> otherwise. Use 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> to retrieve the error code. ERROR_NOT_CONNECTED is returned by 
<b>GetLastError</b> if a connection cannot be made or if the sockets database is unconditionally offline.




## -remarks



<b>InternetCheckConnection</b> is deprecated. <b>InternetCheckConnection</b> does not work in environments that use a web proxy server to access the Internet. Depending on the environment, use  <a href="https://go.microsoft.com/fwlink/p/?linkid=861634">NetworkInformation.GetInternetConnectionProfile</a> or the <a href="https://msdn.microsoft.com/57cc2a07-4551-428c-a303-9b1a4510f225">NLM Interfaces</a> to check for Internet access instead.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/80747c0d-5a09-4ffa-a0ca-b051b82acbf8">Enabling Internet Functionality</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

