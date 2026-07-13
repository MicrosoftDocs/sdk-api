---
UID: NF:ws2tcpip.gai_strerrorA
title: gai_strerrorA function (ws2tcpip.h)
description: The gai_strerror function assists in printing error messages based on the EAI_* errors returned by the getaddrinfo function. (ANSI)
helpviewer_keywords: ["gai_strerrorA", "ws2tcpip/gai_strerrorA"]
old-location: winsock\gai_strerror_2.htm
tech.root: WinSock
ms.assetid: 00b4c5de-89c9-419f-bff8-822ef0446697
ms.date: 12/05/2018
ms.keywords: _win32_gai_strerror_2, gai_strerror, gai_strerror function [Winsock], gai_strerrorA, gai_strerrorW, winsock.gai_strerror_2, ws2tcpip/gai_strerror, ws2tcpip/gai_strerrorA, ws2tcpip/gai_strerrorW, wspiapi/gai_strerror, wspiapi/gai_strerrorA, wspiapi/gai_strerrorW
req.header: ws2tcpip.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: gai_strerrorW (Unicode) and gai_strerrorA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - gai_strerrorA
 - ws2tcpip/gai_strerrorA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ws2tcpip.h
 - Wspiapi.h
api_name:
 - gai_strerror
 - gai_strerrorA
 - gai_strerrorW
---

# gai_strerrorA function


## -description

The 
<b>gai_strerror</b> function assists in printing error messages based on the EAI_* errors returned by the 
<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo">getaddrinfo</a> function. Note that the 
<b>gai_strerror</b> function is not thread safe, and therefore, use of traditional Windows Sockets functions such as the 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a> function is recommended.

## -parameters

### -param ecode [in]

Error code from the list of available 
<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo">getaddrinfo</a> error codes. For a complete listing of error codes, see the 
<b>getaddrinfo</b> function.

## -returns

Returns a pointer to a string containing the error message.

## -remarks

If the <i>ecode</i> parameter is not an error code value that 
<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo">getaddrinfo</a> returns, the 
<b>gai_strerror</b> function returns a pointer to a string that indicates an unknown error.





> [!NOTE]
> The ws2tcpip.h header defines gai_strerror as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo">getaddrinfo</a>
