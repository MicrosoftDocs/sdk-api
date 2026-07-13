---
UID: NF:winsock2.htonll
title: htonll function (winsock2.h)
description: Converts an unsigned __int64 from host to TCP/IP network byte order (which is big-endian).
helpviewer_keywords: ["htonll","htonll function [Winsock]","winsock.htonll","winsock2/htonll"]
old-location: winsock\htonll.htm
tech.root: WinSock
ms.assetid: 3155C55D-681E-4D6D-9DFF-219465F04E4A
ms.date: 12/05/2018
ms.keywords: htonll, htonll function [Winsock], winsock.htonll, winsock2/htonll
req.header: winsock2.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - htonll
 - winsock2/htonll
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winsock2.h
api_name:
 - htonll
---

# htonll function


## -description

The 
<b>htonll</b> inline function converts an <b>unsigned __int64</b> from host to TCP/IP network byte order (which is big-endian).

## -parameters

### -param Value

A 64-bit unsigned number in host byte order.

## -returns

The 
<b>htonll</b> function returns the value in TCP/IP's network byte order.

## -remarks

The 
<b>htonll</b> inline function takes a 64-bit number in host byte order and returns a 64-bit number in the network byte order used in TCP/IP networks (the AF_INET or AF_INET6 address family).

The 
<b>htonll</b> inline function can be used to convert an IPv4 address in host byte order to the IPv4 address in network byte order. This function does not do any checking to determine if the <i>value</i> parameter is a valid IPv4 address.

The <b>htonll</b> inline function does not require that the Winsock DLL has previously been loaded with a successful 
call to the <a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a> function.

<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

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



<a href="/windows/desktop/api/winsock/nf-winsock-htons">htons</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_addr">inet_addr</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_ntoa">inet_ntoa</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-ntohd">ntohd</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-ntohf">ntohf</a>



<a href="/windows/desktop/api/winsock/nf-winsock-ntohl">ntohl</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-ntohll">ntohll</a>



<a href="/windows/desktop/api/winsock/nf-winsock-ntohs">ntohs</a>