---
UID: NF:ip2string.RtlIpv4StringToAddressExW
title: RtlIpv4StringToAddressExW function (ip2string.h)
description: Converts a string representation of an IPv4 address and port number to a binary IPv4 address and port. (Unicode)
helpviewer_keywords: ["RtlIpv4StringToAddressEx", "RtlIpv4StringToAddressEx function [IP Helper]", "RtlIpv4StringToAddressExW", "ip2string/RtlIpv4StringToAddressEx", "ip2string/RtlIpv4StringToAddressExW", "iphlp.rtlipv4stringtoaddressex"]
old-location: iphlp\rtlipv4stringtoaddressex.htm
tech.root: IpHlp
ms.assetid: 72d20cf0-38ff-4c00-93ec-949aaf6f96e2
ms.date: 12/05/2018
ms.keywords: RtlIpv4StringToAddressEx, RtlIpv4StringToAddressEx function [IP Helper], RtlIpv4StringToAddressExW, ip2string/RtlIpv4StringToAddressEx, ip2string/RtlIpv4StringToAddressExW, iphlp.rtlipv4stringtoaddressex
req.header: ip2string.h
req.include-header: Mstcpip.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RtlIpv4StringToAddressExW (Unicode) and RtlIpv4StringToAddressEx (ANSI)
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
 - RtlIpv4StringToAddressExW
 - ip2string/RtlIpv4StringToAddressExW
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
 - RtlIpv4StringToAddressEx
 - RtlIpv4StringToAddressEx
 - RtlIpv4StringToAddressExW
---

# RtlIpv4StringToAddressExW function


## -description

The 
<b>RtlIpv4StringToAddressEx</b> function  converts a string representation of an IPv4 address and port number to a binary IPv4 address and port.

## -parameters

### -param AddressString [in]

A pointer to a buffer containing the <b>NULL</b>-terminated string representation of the IPv4 address followed by an optional colon and string representation of a port number.

### -param Strict [in]

A value that indicates whether the string must be an IPv4 address represented in strict four-part dotted-decimal notation.  If this parameter is <b>TRUE</b>, the string must be dotted-decimal with four parts. If this parameter is <b>FALSE</b>, any of four forms are allowed for the string representation of the Ipv4 address, with decimal,
             octal, or hexadecimal notation. See the Remarks section for details.

### -param Address [out]

A pointer where the binary representation of the IPv4 address is to be stored. The IPv4 address is stored in network byte order.

### -param Port [out]

A pointer where the binary representation of the port number is to be stored. The port number is returned in network byte order. If no port was specified in the string pointed to by the <i>AddressString</i> parameter, then the <i>Port</i> parameter is set to zero.

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
An invalid parameter was passed to the function. This error is returned if the <i>Strict</i> parameter was set to <b>TRUE</b>, but the string pointed to by the <i>AddressString</i> parameter did not contain a four-part dotted-decimal string representation of an IPv4 address. This error is also returned if the string pointed to by the  <i>AddressString</i> parameter did not contain a proper string representation of an IPv4 address.

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
Use 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>

## -remarks

The <b>RtlIpv4StringToAddressEx</b> function is used to convert a string representation of the IPv4 address and port number to a binary IPv4 address and a port number. The IPv4 address is returned in network order (bytes ordered from
    left to right). The port number is returned in network order. 

<b>RtlIpv4StringToAddressEx</b> is a convenience function that does not require that the Windows Sockets DLL be loaded to access a function provided in Windows Sockets to perform string to IP address conversion. 

If the <i>Strict</i> parameter is set to <b>TRUE</b>, then the string pointed to by the <i>AddressString</i> parameter must be in strict dotted-decimal notation. This strict format requires that four parts are specified. Each part is interpreted as a decimal byte of data
    and assigned, from left to right, to the four bytes of an IPv4
    address.   

When the <i>Strict</i> parameter is set to <b>FALSE</b>, the string pointed to by the <i>AddressString</i> parameter may be in any of the several possible formats. When the buffer pointed to by <i>AddressString</i> parameter contains a three-part address string, the last part is interpreted
    as a 16-bit quantity and placed in the right most two bytes of the
    network address.  This makes the three-part address format
    convenient for specifying Class B network addresses as
    "128.net.host". When the buffer pointed to by <i>AddressString</i> parameter contains a two-part address string, the last part is interpreted
    as a 24-bit quantity and placed in the right most three bytes of the
    network address.  This makes the two part address format convenient
    for specifying Class A network addresses as "net.host". When the buffer pointed to by <i>AddressString</i> parameter contains only a one-part address string, the value is stored directly in the
    network address without any byte rearrangement.


 

The buffer pointed to by the <i>AddressString</i> parameter may contain the IPv4 address string followed by an optional  colon and the string representation of a  port number. If a port number string is included in the buffer pointed to by <i>AddressString</i> parameter, the binary representation of the port number is returned in the <i>Port</i> parameter. If the buffer pointed to by <i>AddressString</i> parameter does not contain a port number, a zero is returned in the <i>Port</i> parameter.  

When either UNICODE or _UNICODE is defined, <b>RtlIpv4StringToAddressEx</b> is defined to <b>RtlIpv4StringToAddressExW</b>, the Unicode version of this function. The <i>AddressString</i> parameter is defined to the PCWSTR data type.



When both UNICODE and  _UNICODE are not defined, <b>RtlIpv4StringToAddressEx</b> is defined to <b>RtlIpv4StringToAddressExA</b>, the ANSI version of this function. The <i>AddressString</i> parameter is defined to the PCSTR data type.



The <a href="/windows/desktop/api/winsock2/ns-winsock2-in_addr">IN_ADDR</a> structure is defined in the <i>Inaddr.h</i> header file.

## -see-also

<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea">GetModuleHandle</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>



<a href="/windows/desktop/api/winsock2/ns-winsock2-in_addr">IN_ADDR</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-inetntopw">InetNtop</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-inetptonw">InetPton</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringa">RtlIpv4AddressToString</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringexw">RtlIpv4AddressToStringEx</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4stringtoaddressa">RtlIpv4StringToAddress</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringa">RtlIpv6AddressToString</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringexw">RtlIpv6AddressToStringEx</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa">RtlIpv6StringToAddress</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6stringtoaddressexw">RtlIpv6StringToAddressEx</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_addr">inet_addr</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_ntoa">inet_ntoa</a>
