---
UID: NF:winsock2.ntohf
title: ntohf function (winsock2.h)
description: Converts an unsigned __int32 from TCP/IP network order to host byte order (which is little-endian on Intel processors) and returns a float.
helpviewer_keywords: ["ntohf","ntohf function [Winsock]","winsock.ntohf","winsock2/ntohf"]
old-location: winsock\ntohf.htm
tech.root: WinSock
ms.assetid: FD98AE9D-C753-479C-BF44-7495B3B5C953
ms.date: 12/05/2018
ms.keywords: ntohf, ntohf function [Winsock], winsock.ntohf, winsock2/ntohf
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
 - ntohf
 - winsock2/ntohf
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
 - ntohf
---

# ntohf function


## -description

The 
<b>ntohf</b> inline function converts an <b>unsigned __int32</b> from TCP/IP network order to host byte order (which is little-endian on Intel processors) and returns a <b>float</b>.

## -parameters

### -param Value

An  <b>unsigned __int32</b> number in TCP/IP network byte order.

## -returns

The 
<b>ntohf</b> function returns the value supplied in the <i>value</i> parameter with the byte order reversed. If  <i>value</i> is already in host byte order, then this function will reverse it. It is up to the application to determine if the byte order must be reversed.

## -remarks

The 
<b>ntohf</b> inline function takes an <b>unsigned __int32</b> in TCP/IP network byte order (the AF_INET or AF_INET6 address family) and returns a <b>float</b> that contains a number in host byte order. 

The 
<b>ntohf</b> function can be used to convert an IPv4 address in network byte order to the IPv4 address in host byte order. This function does not do any checking to determine if the <i>value</i> parameter is a valid IPv4 address.

The <b>ntohf</b> function does not require that the Winsock DLL has previously been loaded with a successful 
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



<a href="/windows/desktop/api/winsock2/nf-winsock2-ntohd">ntohd</a>



<a href="/windows/desktop/api/winsock/nf-winsock-ntohl">ntohl</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-ntohll">ntohll</a>



<a href="/windows/desktop/api/winsock/nf-winsock-ntohs">ntohs</a>