---
UID: NF:ws2tcpip.InetNtopW
title: InetNtopW function (ws2tcpip.h)
description: The InetNtop function converts an IPv4 or IPv6 Internet network address into a string in Internet standard format. The ANSI version of this function is inet_ntop. (InetNtopW)
helpviewer_keywords: ["AF_INET","AF_INET6","InetNtop","InetNtop function [Winsock]","InetNtopA","InetNtopA or inet_ntop","InetNtopW","inet_ntop","winsock.inet_ntop","ws2tcpip/InetNtop","ws2tcpip/InetNtopA or inet_ntop","ws2tcpip/InetNtopW"]
old-location: winsock\inet_ntop.htm
tech.root: WinSock
ms.assetid: 1e26b88c-808f-4807-8641-e5c6b10853ad
ms.date: 12/05/2018
ms.keywords: AF_INET, AF_INET6, InetNtop, InetNtop function [Winsock], InetNtopA, InetNtopA or inet_ntop, InetNtopW, inet_ntop, winsock.inet_ntop, ws2tcpip/InetNtop, ws2tcpip/InetNtopA or inet_ntop, ws2tcpip/InetNtopW
req.header: ws2tcpip.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: InetNtopW (Unicode) and InetNtopA or inet_ntop (ANSI)
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
 - InetNtopW
 - ws2tcpip/InetNtopW
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
 - InetNtop
 - InetNtopA or inet_ntop
 - InetNtopW
---

# InetNtopW function


## -description

The 
<b>InetNtop</b> function converts an IPv4 or IPv6 Internet network address into a string in Internet standard format. The ANSI version of this function is   <b>inet_ntop</b>.

## -parameters

### -param Family [in]

The address family.

Possible values for the address family are defined in the <i>Ws2def.h</i> header file. Note that the <i>Ws2def.h</i> header file is automatically included in <i>Winsock2.h</i>, and should never be used directly. Note that the values for the AF_ address family and PF_ protocol family constants  are identical (for example, <b>AF_INET</b> and <b>PF_INET</b>), so either constant can be used.

The values currently supported are <b>AF_INET</b> and <b>AF_INET6</b>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AF_INET"></a><a id="af_inet"></a><dl>
<dt><b>AF_INET</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The Internet Protocol version 4 (IPv4) address family. When this parameter is specified,  this function  returns an IPv4 address string.

</td>
</tr>
<tr>
<td width="40%"><a id="AF_INET6"></a><a id="af_inet6"></a><dl>
<dt><b>AF_INET6</b></dt>
<dt>23</dt>
</dl>
</td>
<td width="60%">
The Internet Protocol version 6 (IPv6) address family. When this parameter is specified,  this function  returns an IPv6 address string.

</td>
</tr>
</table>

### -param pAddr [in]

A pointer to the IP address in network byte to convert to a string.

When the <i>Family</i> parameter is <b>AF_INET</b>, then the <i>pAddr</i> parameter must point to an <a href="/windows/desktop/api/winsock2/ns-winsock2-in_addr">IN_ADDR</a> structure with the IPv4 address to convert.

When the <i>Family</i> parameter is <b>AF_INET6</b>, then the <i>pAddr</i> parameter must point to an <a href="/previous-versions/windows/desktop/legacy/ms738560(v=vs.85)">IN6_ADDR</a> structure with the IPv6 address to convert.

### -param pStringBuf [out]

A pointer to a buffer in which to store the <b>NULL</b>-terminated string representation of the IP address.

For an IPv4 address, this buffer should be large enough to hold at least 16 characters.

For an IPv6 address, this buffer should be large enough to hold at least 46 characters.

### -param StringBufSize [in]

On input, the length, in characters, of the buffer pointed to by the <i>pStringBuf</i> parameter.

## -returns

If no error occurs, 
<b>InetNtop</b> function returns a pointer to a buffer containing the string representation of IP address in standard format.

Otherwise, a value of <b>NULL</b> is returned, and a specific error code can be retrieved by calling the  
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a> for extended error information.

If the function fails, the extended error code returned by <a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a> can be one of the following values.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEAFNOSUPPORT</a></b></dt>
</dl>
</td>
<td width="60%">
The address family specified in the <i>Family</i> parameter is not supported. This error is returned if the <i>Family</i> parameter specified was not <b>AF_INET</b> or <b>AF_INET6</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function. This error is returned if a <b>NULL</b> pointer is passed in the <i>pStringBuf</i> or the  <i>StringBufSize</i> parameter is zero. This error is also returned if the length of the buffer pointed to by the <i>pStringBuf</i> parameter is not large enough to receive the string representation of the IP address.

</td>
</tr>
</table>

## -remarks

The 
<b>InetNtop</b> function is supported on Windows Vista and later.

The 
<b>InetNtop</b> function provides a protocol-independent address-to-string translation. The 
<b>InetNtop</b> function takes an Internet address structure specified by the <i>pAddr</i> parameter and returns a <b>NULL</b>-terminated string that represents the IP address. While the <a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_ntoa">inet_ntoa</a> function works only with IPv4 addresses, the <b>InetNtop</b> function works with either IPv4 or IPv6 addresses.

The ANSI version of this function is <b>inet_ntop</b> as defined in RFC 2553. For more information, see RFC 2553 available at the <a href="http://tools.ietf.org/html/rfc2553">IETF website</a>. 

The 
<b>InetNtop</b> function does not require that the Windows Sockets DLL be loaded to perform IP address to string conversion.

If the <i>Family</i> parameter specified is <b>AF_INET</b>, then the <i>pAddr</i> parameter must point to an <a href="/windows/desktop/api/winsock2/ns-winsock2-in_addr">IN_ADDR</a> structure with the IPv4 address to convert. The address string returned in the buffer pointed to by the <i>pStringBuf</i> parameter is  in dotted-decimal notation as in "192.168.16.0", an example of an IPv4 address in dotted-decimal notation.

If the <i>Family</i> parameter specified is <b>AF_INET6</b>, then the <i>pAddr</i> parameter must point to an <a href="/previous-versions/windows/desktop/legacy/ms738560(v=vs.85)">IN6_ADDR</a> structure with the IPv6 address to convert. The address string returned in the buffer pointed to by the <i>pStringBuf</i> parameter is in Internet standard format. The basic string representation consists of 8 hexadecimal numbers separated by colons. A string of consecutive zero numbers is replaced with a double-colon. There can only be one double-colon in the string representation of the IPv6 address. The last 32 bits are represented in IPv4-style dotted-octet notation if the address is a IPv4-compatible address.

If the length of the buffer pointed to by the <i>pStringBuf</i> parameter is not large enough to receive the string representation of the IP address, <b>InetNtop</b> returns ERROR_INVALID_PARAMETER.

When UNICODE or _UNICODE is defined, <b>InetNtop</b> is defined to <b>InetNtopW</b>, the Unicode version of this function. The <i>pStringBuf</i> parameter is defined to the <b>PWSTR</b> data type.

When UNICODE or _UNICODE is not defined, <b>InetNtop</b> is defined to <b>InetNtopA</b>, the ANSI version of this function. The ANSI version of this function is always defined as <b>inet_ntop</b>. The <i>pStringBuf</i> parameter is defined to the <b>PSTR</b> data type.

The <a href="/windows/desktop/api/winsock2/ns-winsock2-in_addr">IN_ADDR</a> structure is defined in the <i>Inaddr.h</i> header file.

The <a href="/previous-versions/windows/desktop/legacy/ms738560(v=vs.85)">IN6_ADDR</a> structure is defined in the <i>In6addr.h</i> header file.

On Windows Vista and later, the <a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringa">RtlIpv4AddressToString</a> and <a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringexw">RtlIpv4AddressToStringEx</a> functions can be used to convert an IPv4 address represented as an <a href="/windows/desktop/api/winsock2/ns-winsock2-in_addr">IN_ADDR</a> structure to a string representation of an IPv4 address in Internet standard dotted-decimal notation. On Windows Vista and later, the <a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringa">RtlIpv6AddressToString</a> and <a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringexw">RtlIpv6AddressToStringEx</a> functions can be used to convert an IPv6 address represented as an <a href="/previous-versions/windows/desktop/legacy/ms738560(v=vs.85)">IN6_ADDR</a> structure to a string representation of an IPv6 address. The <b>RtlIpv6AddressToStringEx</b> function is more flexible since it also converts an IPv6 address, scope ID, and port to a IPv6 string in standard format.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: The  <b>InetNtopW</b> function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/ms738560(v=vs.85)">IN6_ADDR</a>



<a href="/windows/desktop/api/winsock2/ns-winsock2-in_addr">IN_ADDR</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-inetptonw">InetPton</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringa">RtlIpv4AddressToString</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringexw">RtlIpv4AddressToStringEx</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4stringtoaddressa">RtlIpv4StringToAddress</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4stringtoaddressexw">RtlIpv4StringToAddressEx</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringa">RtlIpv6AddressToString</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringexw">RtlIpv6AddressToStringEx</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa">RtlIpv6StringToAddress</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6stringtoaddressexw">RtlIpv6StringToAddressEx</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_addr">inet_addr</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_ntoa">inet_ntoa</a>
