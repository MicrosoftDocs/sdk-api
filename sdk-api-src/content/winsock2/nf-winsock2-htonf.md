---
UID: NF:winsock2.htonf
title: htonf function (winsock2.h)
description: Converts a float from host to TCP/IP network byte order (which is big-endian).
helpviewer_keywords: ["htonf","htonf function [Winsock]","winsock.htonf","winsock2/htonf"]
old-location: winsock\htonf.htm
tech.root: WinSock
ms.assetid: 93011B2E-2B3C-4EDD-90F7-82A11542A154
ms.date: 12/05/2018
ms.keywords: htonf, htonf function [Winsock], winsock.htonf, winsock2/htonf
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
 - htonf
 - winsock2/htonf
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
 - htonf
---

# htonf function


## -description

The 
<b>htonf</b> inline function converts a <b>float</b> from host to TCP/IP network byte order (which is big-endian).

## -parameters

### -param Value

A float that contains a number in host byte order.

## -returns

The 
<b>htonf</b> function returns the value in TCP/IP's network byte order.

## -remarks

The 
<b>htonf</b> inline function takes a <b>float</b> that contains number in host byte order and returns a 32-bit unsigned number in the network byte order used in TCP/IP networks (the AF_INET or AF_INET6 address family).

The 
<b>htonf</b> inline function can be used to convert an IPv4 address in host byte order to the IPv4 address in network byte order. This function does not do any checking to determine if the <i>value</i> parameter is a valid IPv4 address.

The <b>htonf</b> inline function does not require that the Winsock DLL has previously been loaded with a successful 
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



<a href="/windows/desktop/api/winsock2/nf-winsock2-htonll">htonll</a>



<a href="/windows/desktop/api/winsock/nf-winsock-htons">htons</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_addr">inet_addr</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_ntoa">inet_ntoa</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-ntohd">ntohd</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-ntohf">ntohf</a>



<a href="/windows/desktop/api/winsock/nf-winsock-ntohl">ntohl</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-ntohll">ntohll</a>



<a href="/windows/desktop/api/winsock/nf-winsock-ntohs">ntohs</a>