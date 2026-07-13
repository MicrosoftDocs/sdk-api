---
UID: NF:ip2string.RtlIpv6StringToAddressA
title: RtlIpv6StringToAddressA function (ip2string.h)
description: Converts a string representation of an IPv6 address to a binary IPv6 address. (ANSI)
helpviewer_keywords: ["RtlIpv6StringToAddressA", "ip2string/RtlIpv6StringToAddressA"]
old-location: iphlp\rtlipv6stringtoaddress.htm
tech.root: IpHlp
ms.assetid: 3cd3bfcf-e9b2-4ee6-8e93-a31a70fc3ad3
ms.date: 12/05/2018
ms.keywords: RtlIpv6StringToAddress, RtlIpv6StringToAddress function [IP Helper], RtlIpv6StringToAddressA, RtlIpv6StringToAddressW, ip2string/RtlIpv6StringToAddress, ip2string/RtlIpv6StringToAddressA, ip2string/RtlIpv6StringToAddressW, iphlp.rtlipv6stringtoaddress
req.header: ip2string.h
req.include-header: Mstcpip.h, Ip2string.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RtlIpv6StringToAddressW (Unicode) and RtlIpv6StringToAddressA (ANSI)
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
 - RtlIpv6StringToAddressA
 - ip2string/RtlIpv6StringToAddressA
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
 - RtlIpv6StringToAddress
 - RtlIpv6StringToAddressA
 - RtlIpv6StringToAddressW
---

# RtlIpv6StringToAddressA function


## -description

The 
<b>RtlIpv6StringToAddress</b> function  converts a string representation of an IPv6 address to a binary IPv6 address.

## -parameters

### -param S [in]

A pointer to a buffer containing the <b>NULL</b>-terminated string representation of the IPv6 address.

### -param Terminator [out]

A parameter that receives a pointer to the character that terminated
        the converted string. This can be used by the caller to extract more information from the string.

### -param Addr [out]

A pointer where the binary representation of the IPv6 address is to be stored.

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
An invalid parameter was passed to the function. This error is returned if the string pointed to by the <i>S</i> parameter did not contain a proper string representation of an IPv6 address.

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

The <b>RtlIpv6StringToAddress</b> function is used to convert a string representation of the IPv6 address to an IPv6 address returned in network order (bytes ordered from
    left to right). 

<b>RtlIpv6StringToAddress</b> is a convenience function that does not require that the Windows Sockets DLL be loaded to access a function provided in Windows Sockets to perform string to IP address conversion. 

The string pointed to by the <i>S</i> parameter must be represented in the form for an IPv6 address string. The basic string representation of an IPv6 address consists of 8 hexadecimal numbers
    separated by colons. A string of consecutive zero numbers may be replaced
    with a double-colon.
    There can only be one double-colon in the string representation of the IPv6 address. The last 32 bits may be represented in IPv4-style dotted-octet notation
    if the address is an IPv4-compatible address, an IPv4-mapped IPv6 address, or an ISATAP address. For more information, see section 5 of <a href="http://tools.ietf.org/html/rfc5952">RFC 5942</a> published by the IETF. 

On success, the <i>Terminator</i> parameter points to the character that terminated the string that was converted. This allows an application to pass a string that contains and IP address plus additional information to the <b>RtlIpv6StringToAddress</b> function and then parse the remaining information. 

<div class="alert"><b>Note</b>  Some malformed IPv6 addresses (::::, for example) start with a valid IPv6 address.  The <b>RtlIpv6StringToAddress</b> function will return success, having parsed the valid part of the IPv6 address as the double colon (::).  The terminator then points to the third colon.  To validate that the entire passed-in string is a valid IPv6 address, you need to ensure that the terminator points to the correct character. If the  <i>S</i> parameter contains only an  IPv6 address, then the terminator should point to the <b>NULL</b> character at the end of the string.</div>
<div> </div>
When either UNICODE or _UNICODE is defined, <b>RtlIpv6StringToAddress</b> is defined to <b>RtlIpv6StringToAddressW</b>, the Unicode version of this function. The <i>S</i> and <i>Terminator</i> parameters are defined to the PCWSTR data type.





When both UNICODE and _UNICODE are not defined, <b>RtlIpv6StringToAddress</b> is defined to <b>RtlIpv6StringToAddressA</b>, the ANSI version of this function. The <i>S</i> and <i>Terminator</i> parameters are defined to the PCSTR data type.



The <a href="/previous-versions/windows/desktop/legacy/ms738560(v=vs.85)">IN6_ADDR</a> structure is defined in the In6addr.h header file.





> [!NOTE]
> The ip2string.h header defines RtlIpv6StringToAddress as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea">GetModuleHandle</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>



<a href="/previous-versions/windows/desktop/legacy/ms738560(v=vs.85)">IN6_ADDR</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-inetntopw">InetNtop</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-inetptonw">InetPton</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringa">RtlIpv4AddressToString</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringexw">RtlIpv4AddressToStringEx</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4stringtoaddressa">RtlIpv4StringToAddress</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4stringtoaddressexw">RtlIpv4StringToAddressEx</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringa">RtlIpv6AddressToString</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringexw">RtlIpv6AddressToStringEx</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6stringtoaddressexw">RtlIpv6StringToAddressEx</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_addr">inet_addr</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_ntoa">inet_ntoa</a>
