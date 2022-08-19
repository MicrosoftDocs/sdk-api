---
UID: NF:winineti.InternetHangUp
title: InternetHangUp function (winineti.h)
description: The InternetHangUp function (winineti.h) instructs the modem to disconnect from the Internet.
helpviewer_keywords: ["InternetHangUp","InternetHangUp function [WinINet]","_inet_internethangup_function","wininet.internethangup","winineti/InternetHangUp"]
old-location: wininet\internethangup.htm
tech.root: wininet
ms.assetid: 5d74532e-14cd-45c1-b16b-b302bed89c12
ms.date: 08/15/2022
ms.keywords: InternetHangUp, InternetHangUp function [WinINet], _inet_internethangup_function, wininet.internethangup, winineti/InternetHangUp
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InternetHangUp
 - winineti/InternetHangUp
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wininet.dll
api_name:
 - InternetHangUp
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

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/WinInet/establishing-a-dial-up-connection-to-the-internet">Establishing a Dial-Up Connection to the Internet</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
