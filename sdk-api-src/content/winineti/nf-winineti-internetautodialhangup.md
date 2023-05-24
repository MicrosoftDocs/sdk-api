---
UID: NF:winineti.InternetAutodialHangup
title: InternetAutodialHangup function (winineti.h)
description: The InternetAutodialHangup function (winineti.h) disconnects an automatic dial-up connection.
helpviewer_keywords: ["InternetAutodialHangup","InternetAutodialHangup function [WinINet]","_inet_internetautodialhangup_function","wininet.internetautodialhangup","winineti/InternetAutodialHangup"]
old-location: wininet\internetautodialhangup.htm
tech.root: wininet
ms.assetid: 8aa8ecb8-cacd-4cd9-a00b-5293b28dd6bf
ms.date: 08/15/2022
ms.keywords: InternetAutodialHangup, InternetAutodialHangup function [WinINet], _inet_internetautodialhangup_function, wininet.internetautodialhangup, winineti/InternetAutodialHangup
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
 - InternetAutodialHangup
 - winineti/InternetAutodialHangup
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
 - InternetAutodialHangup
---

# InternetAutodialHangup function


## -description

Disconnects an automatic dial-up connection.

## -parameters

### -param dwReserved [in]

This parameter is reserved and must be 0.

## -returns

If the function succeeds, it returns <b>TRUE</b>.


If the function fails, it returns <b>FALSE</b>. Applications can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> to retrieve the error code.

## -remarks

<b>InternetAutoDialHangup</b> returns <b>TRUE</b> if autodial is not enabled, or if autodial is enabled but does not have an entry configured on the computer.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/WinInet/establishing-a-dial-up-connection-to-the-internet">Establishing a Dial-Up Connection to the Internet</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
