---
UID: NF:ip2string.RtlIpv6StringToAddressExA
tech.root: IpHlp 
title: RtlIpv6StringToAddressExA
ms.date: 04/14/2021
targetos: Windows
description: Converts a string representation of an IPv6 address, scope ID, and port number to a binary IPv6 address, scope ID, and port. (ANSI)
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Ntdll.dll 
req.header: ip2string.h
req.idl: 
req.include-header: Mstcpip.h 
req.irql: 
req.kmdf-ver: 
req.lib: ntdll.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps] 
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps] 
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - Ntdll.dll
api_name:
 - RtlIpv6StringToAddressExA
 - RtlIpv6StringToAddressEx
f1_keywords:
 - RtlIpv6StringToAddressExA
 - ip2string/RtlIpv6StringToAddressExA
 - RtlIpv6StringToAddressEx
 - ip2string/RtlIpv6StringToAddressEx
dev_langs:
 - c++
---

# RtlIpv6StringToAddressExA function

## -description

The <b>RtlIpv6StringToAddressEx</b> function  converts a string representation of an IPv6 address, scope ID, and port number to a binary IPv6 address, scope ID, and port.

## -parameters

### -param AddressString [in]

A pointer to a buffer containing the <b>NULL</b>-terminated string representation of the IPv6 address, scope ID, and port number.

### -param Address [out]

A pointer where the binary representation of the IPv6 address is to be stored.

### -param ScopeId [out]

A pointer to where scope ID of the IPv6 address is stored. If <i>AddressString</i> parameter does not contain the string representation of a scope ID, then zero is returned in this parameter.

### -param Port [out]

A pointer where the port number is stored. The port number is in network byte order format. If <i>AddressString</i> parameter does not contain the string representation of a port number, then zero is returned in this parameter.

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
An invalid parameter was passed to the function. This error is returned if the string pointed to by the  <i>AddressString</i> parameter did not contain a proper string representation of an IPv6 address.

This error code is defined in the Ntstatus.h header file.
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
Use <a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to obtain the message string for the returned error.
</td>
</tr>
</table>

## -remarks

The <b>RtlIpv6StringToAddressEx</b> function is used to convert a string representation of the IPv6 address, scope ID, and port number to a binary IPv6 address, scope ID, and port number.  The IPv6 address is returned in network order (bytes ordered from left to right). The port number and scope ID are returned in network order.

<b>RtlIpv6StringToAddressEx</b> is a convenience function that does not require that the Windows Sockets DLL be loaded to access a function provided in Windows Sockets to perform string to IP address conversion.

The string pointed to by the <i>AddressString</i> parameter must be represented in the form for an IPv6 address string followed by an optional percent character and scope ID string. The IPv6 address and scope ID string must be enclosed  in square brackets. The right square bracket after the IPv6 address and scope ID  string may be followed by an optional colon and a string representation of a port number. The basic string representation of an IPv6 address consists of 8 hexadecimal numbers separated by colons. A string of consecutive zero numbers may be replaced with a double-colon. There can only be one double-colon in the string representation of the IPv6 address. The last 32 bits may be represented in IPv4-style dotted-octet notation if the address is an IPv4-compatible address, an IPv4-mapped IPv6 address, or an ISATAP address. For more information, see section 5 of <a href="http://tools.ietf.org/html/rfc5952">RFC 5942</a> published by the IETF.

When either UNICODE or _UNICODE is defined, <b>RtlIpv6StringToAddressEx</b> is defined to <b>RtlIpv6StringToAddressExW</b>, the Unicode version of this function. The <i>AddressString</i> parameter is defined to the PCWSTR data type.

When both UNICODE and _UNICODE are not defined, <b>RtlIpv6StringToAddressEx</b> is defined to <b>RtlIpv6StringToAddressExA</b>, the ANSI version of this function. The <i>AddressString</i> parameter is defined to the PCSTR data type.

The <a href="/previous-versions/windows/desktop/legacy/ms738560(v=vs.85)">IN6_ADDR</a> structure is defined in the In6addr.h header file.

## -see-also

<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea">GetModuleHandle</a>  
<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>  
<a href="/previous-versions/windows/desktop/legacy/ms738560(v=vs.85)">IN6_ADDR</a>  
<a href="/windows/win32/api/ws2tcpip/nf-ws2tcpip-inet_ntop">InetNtop</a>  
<a href="/windows/win32/api/ws2tcpip/nf-ws2tcpip-inet_pton">InetPton</a>  
<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a>  
<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringa">RtlIpv4AddressToString</a>  
<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringexa">RtlIpv4AddressToStringEx</a>  
<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4stringtoaddressa">RtlIpv4StringToAddress</a>  
<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4stringtoaddressexa">RtlIpv4StringToAddressEx</a>  
<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringa">RtlIpv6AddressToString</a>  
<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringexa">RtlIpv6AddressToStringEx</a>  
<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa">RtlIpv6StringToAddress</a>  
<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_addr">inet_addr</a>  
<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_ntoa">inet_ntoa</a>  
