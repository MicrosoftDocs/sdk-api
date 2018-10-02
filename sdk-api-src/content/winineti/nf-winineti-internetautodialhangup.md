---
UID: NF:winineti.InternetAutodialHangup
title: InternetAutodialHangup function
author: windows-sdk-content
description: Disconnects an automatic dial-up connection.
old-location: wininet\internetautodialhangup.htm
tech.root: WinInet
ms.assetid: 8aa8ecb8-cacd-4cd9-a00b-5293b28dd6bf
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: InternetAutodialHangup, InternetAutodialHangup function [WinINet], _inet_internetautodialhangup_function, wininet.internetautodialhangup, winineti/InternetAutodialHangup
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - InternetAutodialHangup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# InternetAutodialHangup function


## -description


Disconnects an automatic dial-up connection.


## -parameters




### -param dwReserved [in]

This parameter is reserved and must be 0.


## -returns



If the function succeeds, it returns <b>TRUE</b>.


If the function fails, it returns <b>FALSE</b>. Applications can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> to retrieve the error code.




## -remarks



<b>InternetAutoDialHangup</b> returns <b>TRUE</b> if autodial is not enabled, or if autodial is enabled but does not have an entry configured on the computer.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/dd33ed4b-eb7c-449c-b309-8f5c290a5a93">Establishing a Dial-Up Connection to the Internet</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

