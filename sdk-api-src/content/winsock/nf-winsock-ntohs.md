---
UID: NF:winsock.ntohs
title: ntohs function (winsock.h)
description: The ntohs function (winsock.h) converts a u_short from TCP/IP network byte order to host byte order, which is little-endian on Intel processors.
helpviewer_keywords: ["_win32_ntohs_2","ntohs","ntohs function [Winsock]","winsock.ntohs_2","winsock/ntohs"]
old-location: winsock\ntohs_2.htm
tech.root: WinSock
ms.assetid: 9946df13-3b40-4bcb-91ca-10684b3fc9a5
ms.date: 08/16/2022
ms.keywords: _win32_ntohs_2, ntohs, ntohs function [Winsock], winsock.ntohs_2, winsock/ntohs
req.header: winsock.h
req.include-header: Winsock2.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - ntohs
 - winsock/ntohs
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
 - ntohs
---

# ntohs function


## -description

The 
<b>ntohs</b> function converts a <b>u_short</b> from TCP/IP network byte order to host byte order (which is little-endian on Intel processors).

## -parameters

### -param netshort [in]

A 16-bit number in TCP/IP network byte order.

## -returns

The 
<b>ntohs</b> function returns the value in host byte order. If the <i>netshort</i> parameter is already in host byte order, then this function will reverse it. It is up to the application to determine if the byte order must be reversed.

## -remarks

The 
<b>ntohs</b> function takes a 16-bit number in TCP/IP network byte order (the AF_INET or AF_INET6 address family) and returns a 16-bit number in host byte order.

The 
<b>ntohs</b> function can be used to convert an IP port number in network byte order to the IP port number in host byte order. 

The <b>ntohs</b> function does not require that the Winsock DLL has previously been loaded with a successful 
call to the <a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a> function.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-inetntopw">InetNtop</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-inetptonw">InetPton</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsahtonl">WSAHtonl</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsahtons">WSAHtons</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsantohl">WSANtohl</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsantohs">WSANtohs</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-htond">htond</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-htonf">htonf</a>



<a href="/windows/desktop/api/winsock/nf-winsock-htonl">htonl</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-htonll">htonll</a>



<a href="/windows/desktop/api/winsock/nf-winsock-htons">htons</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_addr">inet_addr</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_ntoa">inet_ntoa</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-ntohd">ntohd</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-ntohf">ntohf</a>



<a href="/windows/desktop/api/winsock/nf-winsock-ntohl">ntohl</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-ntohll">ntohll</a>
