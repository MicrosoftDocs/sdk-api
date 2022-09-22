---
UID: NF:winsock2.inet_ntoa
title: inet_ntoa function (winsock2.h)
description: The inet_ntoa function (winsock2.h) converts an (Ipv4) Internet network address into an ASCII string in Internet standard dotted-decimal format.  
helpviewer_keywords: ["_win32_inet_ntoa_2","inet_ntoa","inet_ntoa function [Winsock]","winsock.inet_ntoa_2","wsipv6ok/inet_ntoa"]
old-location: winsock\inet_ntoa_2.htm
tech.root: WinSock
ms.assetid: 01cd32e7-a01d-40e8-afb5-69223d643a0e
ms.date: 08/03/2022
ms.keywords: _win32_inet_ntoa_2, inet_ntoa, inet_ntoa function [Winsock], winsock.inet_ntoa_2, wsipv6ok/inet_ntoa
req.header: winsock2.h
req.include-header: Winsock2.h, Winsock.h
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
 - inet_ntoa
 - winsock2/inet_ntoa
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
 - inet_ntoa
---

# inet_ntoa function


## -description

The 
<b>inet_ntoa</b> function converts an (Ipv4) Internet network address into an ASCII string in Internet standard dotted-decimal format.

## -parameters

### -param in

TBD




#### - a [in]

An 
<a href="/windows/desktop/api/winsock2/ns-winsock2-in_addr">in_addr</a> structure that represents an Internet host address.

## -returns

If no error occurs, 
<b>inet_ntoa</b> returns a character pointer to a static buffer containing the text address in standard ".'' notation. Otherwise, it returns <b>NULL</b>.

## -remarks

The 
<b>inet_ntoa</b> function takes an Internet address structure specified by the <i>in</i> parameter and returns a <b>NULL</b>-terminated ASCII string that represents the address in "." (dot) notation as in "192.168.16.0", an example of an IPv4 address in dotted-decimal notation.   The string returned by 
<b>inet_ntoa</b> resides in memory that is allocated by Windows Sockets. The application should not make any assumptions about the way in which the memory is allocated. The string returned is guaranteed to be valid only until the next Windows Sockets function call is made within the same thread. Therefore, the data should be copied before another Windows Sockets call is made.

The 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa">WSAAddressToString</a> function can be used to convert a <a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure containing an IPv4 address to a string representation of an IPv4 address in Internet standard dotted-decimal notation. The advantage of the <b>WSAAddressToString</b>  function is that it supports both IPv4 and IPv6 addresses. Another advantage of the  <b>WSAAddressToString</b>  function is that there are both ASCII and Unicode versions of this function.

On Windows Vista and later, the <a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringa">RtlIpv4AddressToString</a> function can be used to convert an IPv4 address represented as an <a href="/windows/desktop/api/winsock2/ns-winsock2-in_addr">IN_ADDR</a> structure to a string representation of an IPv4 address in Internet standard dotted-decimal notation. On Windows Vista and later, the <a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringa">RtlIpv6AddressToString</a> function can be used to convert an IPv6 address represented as an <b>IN6_ADDR</b> structure to a string representation of an IPv6 address. 

<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<b>IN6_ADDR</b>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-inetntopw">InetNtop</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringa">RtlIpv4AddressToString</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringexw">RtlIpv4AddressToStringEx</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4stringtoaddressa">RtlIpv4StringToAddress</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4stringtoaddressexw">RtlIpv4StringToAddressEx</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringa">RtlIpv6AddressToString</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringexw">RtlIpv6AddressToStringEx</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa">RtlIpv6StringToAddress</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6stringtoaddressexw">RtlIpv6StringToAddressEx</a>



<a href="/windows/desktop/WinSock/sockaddr-2">SOCKADDR</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa">WSAAddressToString</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>



<a href="/windows/desktop/api/winsock2/ns-winsock2-in_addr">in_addr</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_addr">inet_addr</a>
