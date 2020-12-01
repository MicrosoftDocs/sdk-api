---
UID: NF:ws2tcpip.GetAddrInfoExCancel
title: GetAddrInfoExCancel function (ws2tcpip.h)
description: Cancels an asynchronous operation by the GetAddrInfoEx function.
helpviewer_keywords: ["GetAddrInfoExCancel","GetAddrInfoExCancel function [Winsock]","winsock.getaddrinfoexcancel","ws2tcpip/GetAddrInfoExCancel"]
old-location: winsock\getaddrinfoexcancel.htm
tech.root: WinSock
ms.assetid: A4DE552D-DEA7-44F5-865F-5B02C9BB4AB6
ms.date: 12/05/2018
ms.keywords: GetAddrInfoExCancel, GetAddrInfoExCancel function [Winsock], winsock.getaddrinfoexcancel, ws2tcpip/GetAddrInfoExCancel
req.header: ws2tcpip.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1, Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetAddrInfoExCancel
 - ws2tcpip/GetAddrInfoExCancel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - GetAddrInfoExCancel
---

# GetAddrInfoExCancel function


## -description

The 
<b>GetAddrInfoExCancel</b> function cancels an asynchronous operation by the <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">GetAddrInfoEx</a> function.

## -parameters

### -param lpHandle [in]

The handle of the asynchronous operation to cancel. This is the handle returned in the <i>lpNameHandle</i> parameter by the <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">GetAddrInfoEx</a> function.

## -returns

On success,  <b>GetAddrInfoExCancel</b> returns <b>NO_ERROR</b> (0). Failure returns a nonzero Windows Sockets error code, as found in the 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">Windows Sockets Error Codes</a>.

## -remarks

The <b>GetAddrInfoExCancel</b> function cancels an asynchronous <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">GetAddrInfoEx</a> operation. The result is that the user's completion
    mechanism, either a callback or an event, is immediately invoked. No results are returned,
    and the error code returned for the <b>GetAddrInfoEx</b> asynchronous operation is set to <b>WSA_E_CANCELLED</b>. If the <b>GetAddrInfoEx</b> request has already completed or timed out,
    or the handle is invalid, and <b>WSA_INVALID_HANDLE</b> will be returned by <b>GetAddrInfoExCancel</b> function.


Since many of the underlying operations (legacy name service providers, for example) are synchronous, these operations
    will not actually be cancelled. These operations will continue running and consuming resources. Once the
    last outstanding name service provider request has completed, the resources will be released. 

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">GetAddrInfoEx</a>