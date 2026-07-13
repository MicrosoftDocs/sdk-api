---
UID: NF:winsock2.ntohd
title: ntohd function (winsock2.h)
description: Converts an unsigned __int64 from TCP/IP network order to host byte order (which is little-endian on Intel processors) and returns a double.
helpviewer_keywords: ["ntohd","ntohd function [Winsock]","winsock.ntohd","winsock2/ntohd"]
old-location: winsock\ntohd.htm
tech.root: WinSock
ms.assetid: 00176446-517B-40B8-AF9A-D61B5B033AE1
ms.date: 12/05/2018
ms.keywords: ntohd, ntohd function [Winsock], winsock.ntohd, winsock2/ntohd
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
 - ntohd
 - winsock2/ntohd
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
 - ntohd
---

# ntohd function


## -description

The 
<b>ntohd</b> inline function converts an <b>unsigned __int64</b> from TCP/IP network order to host byte order (which is little-endian on Intel processors) and returns a  <b>double</b>.

## -parameters

### -param Value

An <b>unsigned __int64</b> number in TCP/IP network byte order.

## -returns

The 
<b>ntohd</b> function returns the value supplied in the <i>value</i> parameter with the byte order reversed. If  <i>value</i> is already in host byte order, then this function will reverse it. It is up to the application to determine if the byte order must be reversed.

## -remarks

The 
<b>ntohd</b> inline function takes an <b>unsigned __int64</b> that contains number in TCP/IP network byte order (the AF_INET or AF_INET6 address family) and returns a <b>double</b>  that contains a number in host byte order. 

The 
<b>ntohd</b> function can be used to convert an IPv4 address in network byte order to the IPv4 address in host byte order. This function does not do any checking to determine if the <i>value</i> parameter is a valid IPv4 address.

The <b>ntohd</b> function does not require that the Winsock DLL has previously been loaded with a successful 
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



<a href="/windows/desktop/api/winsock2/nf-winsock2-htonll">htonll</a>



<a href="/windows/desktop/api/winsock/nf-winsock-htons">htons</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_addr">inet_addr</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_ntoa">inet_ntoa</a>



<a href="/windows/desktop/api/winsock/nf-winsock-ntohl">ntohl</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-ntohll">ntohll</a>



<a href="/windows/desktop/api/winsock/nf-winsock-ntohs">ntohs</a>