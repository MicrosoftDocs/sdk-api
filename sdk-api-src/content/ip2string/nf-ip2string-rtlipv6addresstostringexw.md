---
UID: NF:ip2string.RtlIpv6AddressToStringExW
title: RtlIpv6AddressToStringExW function (ip2string.h)
description: Converts an IPv6 address, scope ID, and port number to a string. (Unicode)
helpviewer_keywords: ["RtlIpv6AddressToStringEx", "RtlIpv6AddressToStringEx function [IP Helper]", "RtlIpv6AddressToStringExW", "ip2string/RtlIpv6AddressToStringEx", "ip2string/RtlIpv6AddressToStringExW", "iphlp.rtlipv6addresstostringex"]
old-location: iphlp\rtlipv6addresstostringex.htm
tech.root: IpHlp
ms.assetid: a7de2da3-21ea-42fa-9474-f33252838632
ms.date: 12/05/2018
ms.keywords: RtlIpv6AddressToStringEx, RtlIpv6AddressToStringEx function [IP Helper], RtlIpv6AddressToStringExW, ip2string/RtlIpv6AddressToStringEx, ip2string/RtlIpv6AddressToStringExW, iphlp.rtlipv6addresstostringex
req.header: ip2string.h
req.include-header: Mstcpip.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RtlIpv6AddressToStringExW (Unicode) and RtlIpv6AddressToStringEx (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: ntdll.lib
req.dll: ntdll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RtlIpv6AddressToStringExW
 - ip2string/RtlIpv6AddressToStringExW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdll.dll
api_name:
 - RtlIpv6AddressToStringEx
 - RtlIpv6AddressToStringEx
 - RtlIpv6AddressToStringExW
---

# RtlIpv6AddressToStringExW function


## -description

The 
<b>RtlIpv6AddressToStringEx</b> function  converts an IPv6 address, scope ID, and port number to a string.

## -parameters

### -param Address [in]

The IPv6 address in network byte order.

### -param ScopeId [in]

The scope ID of the IPv6 address in network byte order. This parameter is optional.

### -param Port [in]

The port number in network byte order format. This parameter is optional.

### -param AddressString [out]

A pointer to the buffer to receive the <b>NULL</b>-terminated string representation of the IP address, scope ID, and port. This buffer should be large enough to hold at least INET6_ADDRSTRLEN characters. The INET6_ADDRSTRLEN value is defined in the <i>Ws2ipdef.h</i> header file.

### -param AddressStringLength [in, out]

On input, the number of characters that fit in the buffer pointed to by the <i>AddressString</i> parameter, including the NULL terminator.
        On output, this parameter contains the number of characters actually written
        to the buffer pointed to by the <i>AddressString</i> parameter.

## -returns

If the function succeeds, the return value is <b>STATUS_SUCCESS</b>.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function. This error is returned if a <b>NULL</b> pointer is passed in the <i>AddressString</i> or <i>AddressStringLength</i> parameter. This error is also returned if the length of the buffer pointed to by the <i>AddressString</i> parameter is not large enough to receive the string representation of the IPv6 address, scope ID, and port. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
Use 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>

## -remarks

The <b>RtlIpv6AddressToStringEx</b> function is used to convert an IPv6 address, scope ID, and port number to the string representation of the IPv6 address in Internet format followed by a string representation of the scope ID followed by a string representation of the port. The scope ID and port number are optional parameters. 

The basic string representation of the IPv6 address returned consists of 8 hexadecimal numbers
    separated by colons. A string of consecutive zero hexadecimal numbers is replaced
    with a double colon.
    There can only be one double colon in the string representation of the IPv6 address. The last 32 bits are represented in IPv4-style dotted-octet notation
    if the address is an IPv4-compatible address, an IPv4-mapped IPv6 address, or an ISATAP address. For more information, see section 5 of <a href="http://tools.ietf.org/html/rfc5952">RFC 5942</a> published by the IETF. 

If a scope ID is provided, the string representation of the scope ID is separated from the string representation of the IPv6 address by a percent character ('%'). If a port number is provided, the string representation of the IPv6 address and the scope ID are surrounded by square braces (a leading '[' character followed by the IPv6 address followed by a '% character followed by the scope ID with a trailing ']' character). The port number is represented as a colon following the right square brace character followed by the string representation of the port number in decimal.

<b>RtlIpv6AddressToStringEx</b> is a convenience function that does not require that the Windows Sockets DLL be loaded to access a function provided in Windows Sockets to perform IP address to string conversion. 

If the length of the buffer pointed to by the <i>AddressString</i> parameter is not large enough to receive the string representation of the IP address, scope ID, and port, <b>RtlIpv6AddressToStringEx</b> returns <b>ERROR_INVALID_PARAMETER</b> and sets the <i>AddressStringLength</i> parameter to the buffer length required. 

When either UNICODE or _UNICODE is defined, <b>RtlIpv6AddressToStringEx</b> is defined to <b>RtlIpv6AddressToStringExW</b>, the Unicode version of this function. The <i>AddressString</i> parameter is defined to the PWSTR data type.



When both UNICODE and _UNICODE are not defined, <b>RtlIpv6AddressToStringEx</b> is defined to <b>RtlIpv6AddressToStringExA</b>, the ANSI version of this function. The <i>AddressString</i> parameter is defined to the PSTR data type.



The <b>IN6_ADDR</b> structure is defined in the <i>In6addr.h</i> header file.

## -see-also

<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea">GetModuleHandle</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-inetntopw">InetNtop</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-inetptonw">InetPton</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringa">RtlIpv4AddressToString</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringexw">RtlIpv4AddressToStringEx</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4stringtoaddressa">RtlIpv4StringToAddress</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4stringtoaddressexw">RtlIpv4StringToAddressEx</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringa">RtlIpv6AddressToString</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa">RtlIpv6StringToAddress</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6stringtoaddressexw">RtlIpv6StringToAddressEx</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_addr">inet_addr</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_ntoa">inet_ntoa</a>
