---
UID: NF:ws2tcpip.gai_strerrorA
title: gai_strerrorA function (ws2tcpip.h)
author: windows-sdk-content
description: The gai_strerror function assists in printing error messages based on the EAI_* errors returned by the getaddrinfo function.
old-location: winsock\gai_strerror_2.htm
tech.root: WinSock
ms.assetid: 00b4c5de-89c9-419f-bff8-822ef0446697
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_win32_gai_strerror_2, gai_strerror, gai_strerror function [Winsock], gai_strerrorA, gai_strerrorW, winsock.gai_strerror_2, ws2tcpip/gai_strerror, ws2tcpip/gai_strerrorA, ws2tcpip/gai_strerrorW, wspiapi/gai_strerror, wspiapi/gai_strerrorA, wspiapi/gai_strerrorW"
ms.topic: function
f1_keywords: 
 - "ws2tcpip/gai_strerror"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# gai_strerrorA function


## -description


The 
<b>gai_strerror</b> function assists in printing error messages based on the EAI_* errors returned by the 
<a href="https://docs.microsoft.com/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo">getaddrinfo</a> function. Note that the 
<b>gai_strerror</b> function is not thread safe, and therefore, use of traditional Windows Sockets functions such as the 
<a href="https://docs.microsoft.com/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a> function is recommended.


## -parameters




### -param ecode [in]

Error code from the list of available 
<a href="https://docs.microsoft.com/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo">getaddrinfo</a> error codes. For a complete listing of error codes, see the 
<b>getaddrinfo</b> function.


## -remarks



If the <i>ecode</i> parameter is not an error code value that 
<a href="https://docs.microsoft.com/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo">getaddrinfo</a> returns, the 
<b>gai_strerror</b> function returns a pointer to a string that indicates an unknown error.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>



<a href="https://docs.microsoft.com/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo">getaddrinfo</a>
 

 

