---
UID: NF:winsock2.htonl
title: htonl function (winsock2.h)
description: The htonl function (winsock2.h) converts a u_long from host to TCP/IP network byte order, which is big-endian.
helpviewer_keywords: ["_win32_htonl_2","htonl","htonl function [Winsock]","winsock.htonl_2","winsock/htonl"]
old-location: winsock\htonl_2.htm
tech.root: WinSock
ms.assetid: e3a18c5e-7efb-43d9-9abc-9d573bbb1923
ms.date: 08/03/2022
ms.keywords: _win32_htonl_2, htonl, htonl function [Winsock], winsock.htonl_2, winsock/htonl
req.header: winsock2.h
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
 - htonl
 - winsock2/htonl
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
 - htonl
---

# htonl function


## -description

The 
<b>htonl</b> function converts a <b>u_long</b> from host to TCP/IP network byte order (which is big-endian).

## -parameters

### -param hostlong [in]

A 32-bit number in host byte order.

## -returns

The 
<b>htonl</b> function returns the value in TCP/IP's network byte order.

## -remarks

The 
<b>htonl</b> function takes a 32-bit number in host byte order and returns a 32-bit number in the network byte order used in TCP/IP networks (the AF_INET or AF_INET6 address family).

The 
<b>htonl</b> function can be used to convert an IPv4 address in host byte order to the IPv4 address in network byte order. This function does not do any checking to determine if the <i>hostlong</i> parameter is a valid IPv4 address.

The <b>htonl</b> function does not require that the Winsock DLL has previously been loaded with a successful 
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



<a href="/windows/desktop/api/winsock2/nf-winsock2-htonll">htonll</a>



<a href="/windows/desktop/api/winsock/nf-winsock-htons">htons</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_addr">inet_addr</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_ntoa">inet_ntoa</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-ntohd">ntohd</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-ntohf">ntohf</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-ntohll">ntohll</a>



<a href="/windows/desktop/api/winsock/nf-winsock-ntohs">ntohs</a>
