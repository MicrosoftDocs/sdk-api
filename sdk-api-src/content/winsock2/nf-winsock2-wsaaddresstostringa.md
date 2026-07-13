---
UID: NF:winsock2.WSAAddressToStringA
title: WSAAddressToStringA function (winsock2.h)
description: Converts all components of a sockaddr structure into a human-readable string representation of the address. (ANSI)
helpviewer_keywords: ["WSAAddressToStringA", "winsock2/WSAAddressToStringA"]
old-location: winsock\wsaaddresstostring_2.htm
tech.root: WinSock
ms.assetid: d72e55e6-79a9-4386-9e1a-24a322f13426
ms.date: 12/05/2018
ms.keywords: WSAAddressToString, WSAAddressToString function [Winsock], WSAAddressToStringA, WSAAddressToStringW, _win32_wsaaddresstostring_2, winsock.wsaaddresstostring_2, winsock2/WSAAddressToString, winsock2/WSAAddressToStringA, winsock2/WSAAddressToStringW
req.header: winsock2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WSAAddressToStringW (Unicode) and WSAAddressToStringA (ANSI)
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
 - WSAAddressToStringA
 - winsock2/WSAAddressToStringA
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
 - WSAAddressToString
 - WSAAddressToStringA
 - WSAAddressToStringW
---

# WSAAddressToStringA function


## -description

The 
<b>WSAAddressToString</b> function converts all components of a 
<a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure into a human-readable string representation of the address.

This is intended to be used mainly for display purposes. If the caller requires that the translation to be performed by a particular provider, it should supply the corresponding 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a> structure in the <i>lpProtocolInfo</i> parameter.

## -parameters

### -param lpsaAddress [in]

A pointer to the 
<a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure to translate into a string.

### -param dwAddressLength [in]

The length, in bytes, of the address in the <a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure pointed to by the <i>lpsaAddress</i> parameter. The <i>dwAddressLength</i> parameter may vary in size with different protocols.

### -param lpProtocolInfo [in, optional]

A pointer to the 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a> structure for a particular provider. If this is parameter is <b>NULL</b>, the call is routed to the provider of the first protocol supporting the address family indicated in the <i>lpsaAddress</i> parameter.

### -param lpszAddressString [in, out]

A pointer to the buffer that receives the human-readable address string.

### -param lpdwAddressStringLength [in, out]

On input, this parameter specifies the length of the buffer pointed to by the <i>lpszAddressString</i> parameter. The length is represented in bytes for ANSI strings, and in WCHARs for Unicode strings. On output, this parameter returns the length of the string including the <b>NULL</b> terminator actually copied into the buffer pointed to by the <i>lpszAddressString</i> parameter. If the specified buffer is not large enough, the function fails with a specific error of 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a> and this parameter is updated with the required size.

## -returns

If no error occurs, 
<b>WSAAddressToString</b> returns a value of zero. Otherwise, the value SOCKET_ERROR is returned, and a specific error number can be retrieved by calling 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The specified <i>lpcsAddress</i>, <i>lpProtocolInfo</i>, and <i>lpszAddressString</i> parameters point to memory that is not all in the address space of the process, or the buffer pointed to by the <i>lpszAddressString</i> parameter is too small. Pass in a larger buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed. This error is returned if the <i>lpsaAddress</i>, <i>dwAddressLength</i>, or <i>lpdwAddressStringLength</i> parameter are <b>NULL</b>. This error is also returned if the specified address is not a valid socket address, or no transport provider supports the indicated address family.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOBUFS</a></b></dt>
</dl>
</td>
<td width="60%">
No buffer space is available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANOTINITIALISED</a></b></dt>
</dl>
</td>
<td width="60%">
The Winsock 2 DLL has not been initialized. The application must first call 
<a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a> before calling any Windows Sockets functions.

</td>
</tr>
</table>

## -remarks

The 
<b>WSAAddressToString</b> function provides a protocol-independent address-to-string translation. The 
<b>WSAAddressToString</b> function takes a socket address structure pointed to by the <i>lpsaAddress</i> parameter and returns a pointer to <b>NULL</b>-terminated string that represents the socket address in the <i>lpszAddressString</i> parameter. While the <a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_ntoa">inet_ntoa</a> function works only with IPv4 addresses, the <b>WSAAddressToString</b> function works with any socket address supported by a Winsock provider on the local computer including IPv6 addresses.

If the <i>lpsaAddress</i> parameter points to an IPv4 socket address (the address family is  <b>AF_INET</b>), then the address string returned in the buffer pointed to by the <i>lpszAddressString</i> parameter is  in dotted-decimal notation as in "192.168.16.0", an example of an IPv4 address in dotted-decimal notation.   

If the <i>lpsaAddress</i> parameter points to an IPv6 socket address (the address family is  <b>AF_INET6</b>), then the address string returned in the buffer pointed to by the <i>lpszAddressString</i> parameter is  in Internet standard format. The basic string representation consists of 8 hexadecimal numbers separated by colons. A string of consecutive zero numbers is replaced with a double-colon. There can only be one double-colon in the string representation of the IPv6 address. 

If the length of the buffer pointed to by the <i>lpszAddressString</i> parameter is not large enough to receive the string representation of the socket address, <b>WSAAddressToString</b> returns 
								<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a>. 

Support for IPv6 addresses using the <b>WSAAddressToString</b> function was added on Windows XP with Service Pack 1 (SP1) and later. IPv6 must also be installed on the local computer for the <b>WSAAddressToString</b> function to support IPv6 addresses. 

<b>Windows Phone 8:</b> The <b>WSAAddressToStringW</b> function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: The <b>WSAAddressToStringW</b> function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.





> [!NOTE]
> The winsock2.h header defines WSAAddressToString as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-inetntopw">InetNtop</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-inetptonw">InetPton</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringa">RtlIpv4AddressToString</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringexw">RtlIpv4AddressToStringEx</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4stringtoaddressa">RtlIpv4StringToAddress</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4stringtoaddressexw">RtlIpv4StringToAddressEx</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringa">RtlIpv6AddressToString</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringexw">RtlIpv6AddressToStringEx</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa">RtlIpv6StringToAddress</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6stringtoaddressexw">RtlIpv6StringToAddressEx</a>



<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsastringtoaddressa">WSAStringToAddress</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_addr">inet_addr</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_ntoa">inet_ntoa</a>



<a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a>
