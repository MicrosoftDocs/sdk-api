---
UID: NF:winineti.InternetHangUp
title: InternetHangUp function
author: windows-sdk-content
description: Instructs the modem to disconnect from the Internet.
old-location: wininet\internethangup.htm
old-project: wininet
ms.assetid: 5d74532e-14cd-45c1-b16b-b302bed89c12
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: InternetHangUp, InternetHangUp function [WinINet], _inet_internethangup_function, wininet.internethangup, winineti/InternetHangUp
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: INTERNET_AUTH_NOTIFY_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wininet.dll
api_name:
 - InternetHangUp
product: Windows
targetos: Windows
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# InternetHangUp function


## -description


Instructs the modem to disconnect from the Internet.


## -parameters




### -param dwConnection [in]

Connection number of  the connection to be disconnected.


### -param dwReserved [in]

This parameter is reserved and must be 0.


## -returns



Returns ERROR_SUCCESS if successful, or an error value otherwise.




## -remarks



<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/dd33ed4b-eb7c-449c-b309-8f5c290a5a93">Establishing a Dial-Up Connection to the Internet</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

