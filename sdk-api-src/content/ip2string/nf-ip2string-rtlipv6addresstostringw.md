---
UID: NF:ip2string.RtlIpv6AddressToStringW
title: RtlIpv6AddressToStringW function (ip2string.h)
description: Converts an IPv6 address to a string in Internet standard format. (Unicode)
helpviewer_keywords: ["RtlIpv6AddressToString", "RtlIpv6AddressToString function [IP Helper]", "RtlIpv6AddressToStringW", "ip2string/RtlIpv6AddressToString", "ip2string/RtlIpv6AddressToStringW", "iphlp.rtlipv6addresstostring"]
old-location: iphlp\rtlipv6addresstostring.htm
tech.root: IpHlp
ms.assetid: a891adb0-6c2d-4b69-a0de-4a615be938e3
ms.date: 12/05/2018
ms.keywords: RtlIpv6AddressToString, RtlIpv6AddressToString function [IP Helper], RtlIpv6AddressToStringA, RtlIpv6AddressToStringW, ip2string/RtlIpv6AddressToString, ip2string/RtlIpv6AddressToStringA, ip2string/RtlIpv6AddressToStringW, iphlp.rtlipv6addresstostring
req.header: ip2string.h
req.include-header: Mstcpip.h, Ip2string.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RtlIpv6AddressToStringW (Unicode) and RtlIpv6AddressToStringA (ANSI)
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
 - RtlIpv6AddressToStringW
 - ip2string/RtlIpv6AddressToStringW
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
 - RtlIpv6AddressToString
 - RtlIpv6AddressToStringA
 - RtlIpv6AddressToStringW
---

# RtlIpv6AddressToStringW function


## -description

The 
<b>RtlIpv6AddressToString</b> function  converts an IPv6 address to a string in Internet standard format.

## -parameters

### -param Addr [in]

The IPv6 address in network byte order.

### -param S [out]

A pointer to a buffer in which to store the <b>NULL</b>-terminated string representation of the IPv6 address. This buffer should be large enough to hold at least 46 characters.

## -returns

A pointer to the NULL character inserted at the end of the string representation of the IPv6 address.
This can be used by the caller to easily append more information to the string.

## -remarks

The <b>RtlIpv6AddressToString</b> function is used to convert an IPv6 address to the string representation of the IPv6 address in Internet standard format. 

The basic string representation consists of 8 hexadecimal numbers
    separated by colons. A string of consecutive zero numbers is replaced
    with a double-colon.
    There can only be one double-colon in the string representation of the IPv6 address. The last 32 bits are represented in IPv4-style dotted-octet notation
    if the address is an IPv4-compatible address, an IPv4-mapped IPv6 address, or an ISATAP address. For more information, see section 5 of <a href="http://tools.ietf.org/html/rfc5952">RFC 5942</a> published by the IETF. 

<b>RtlIpv6AddressToString</b> is a convenience function that does not require that the Windows Sockets DLL be loaded to access a function provided in Windows Sockets to perform IP address to string conversion. 

When either UNICODE or _UNICODE is defined, <b>RtlIpv6AddressToString</b> is defined to <b>RtlIpv6AddressToStringW</b>, the Unicode version of this function. The string parameter <i>S</i> and the function return value are defined to the PWSTR data type.



When both UNICODE and _UNICODE are not defined, <b>RtlIpv6AddressToString</b> is defined to <b>RtlIpv6AddressToStringA</b>, the ANSI version of this function. The string parameter <i>S</i> and the function return value are defined to the PSTR data type.



The <b>IN6_ADDR</b> structure is defined in the <i>In6addr.h</i> header file.



> [!NOTE]
> The ip2string.h header defines RtlIpv6AddressToString as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

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



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringexw">RtlIpv6AddressToStringEx</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa">RtlIpv6StringToAddress</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6stringtoaddressexw">RtlIpv6StringToAddressEx</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_addr">inet_addr</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_ntoa">inet_ntoa</a>
