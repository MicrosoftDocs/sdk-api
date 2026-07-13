---
UID: NF:ip2string.RtlIpv4AddressToStringA
title: RtlIpv4AddressToStringA function (ip2string.h)
description: Converts an IPv4 address to a string in Internet standard dotted-decimal format. (ANSI)
helpviewer_keywords: ["RtlIpv4AddressToStringA", "ip2string/RtlIpv4AddressToStringA"]
old-location: iphlp\rtlipv4addresstostring.htm
tech.root: IpHlp
ms.assetid: f198b770-9429-4b51-9fb4-06cf9917bc21
ms.date: 12/05/2018
ms.keywords: RtlIpv4AddressToString, RtlIpv4AddressToString function [IP Helper], RtlIpv4AddressToStringA, RtlIpv4AddressToStringW, ip2string/RtlIpv4AddressToString, ip2string/RtlIpv4AddressToStringA, ip2string/RtlIpv4AddressToStringW, iphlp.rtlipv4addresstostring
req.header: ip2string.h
req.include-header: Mstcpip.h, Ip2string.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RtlIpv4AddressToStringW (Unicode) and RtlIpv4AddressToStringA (ANSI)
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
 - RtlIpv4AddressToStringA
 - ip2string/RtlIpv4AddressToStringA
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
 - RtlIpv4AddressToString
 - RtlIpv4AddressToStringA
 - RtlIpv4AddressToStringW
---

# RtlIpv4AddressToStringA function


## -description

The 
<b>RtlIpv4AddressToString</b> function  converts an IPv4 address to a string in Internet standard dotted-decimal format.

## -parameters

### -param Addr [in]

The IPv4 address in network byte order.

### -param S [out]

A pointer to a buffer in which to store the <b>NULL</b>-terminated string representation of the IPv4 address. This buffer should be large enough to hold at least 16 characters.

## -returns

A pointer to the NULL character inserted at the end of the string representation of the IPv4 address.
This can be used by the caller to easily append more information to the string.

## -remarks

The <b>RtlIpv4AddressToString</b> function is used to convert an IPv4 address to the string representation of the IPv4 address in Internet dotted-decimal format. 

<b>RtlIpv4AddressToString</b> is a convenience function that does not require that the Windows Sockets DLL be loaded to access a function provided in Windows Sockets to perform IP address to string conversion. 

When either UNICODE or _UNICODE is defined, <b>RtlIpv4AddressToString</b> is defined to <b>RtlIpv4AddressToStringW</b>, the Unicode version of this function. The string parameter <i>S</i> and the function return value are defined to the PWSTR data type.



When both UNICODE and _UNICODE are not defined, <b>RtlIpv4AddressToString</b> is defined to <b>RtlIpv4AddressToStringA</b>, the ANSI version of this function. The string parameter <i>S</i> and the function return value are defined to the PSTR data type.



The <b>IN_ADDR</b> structure is defined in the <i>Inaddr.h</i> header file.



> [!NOTE]
> The ip2string.h header defines RtlIpv4AddressToString as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea">GetModuleHandle</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-inetntopw">InetNtop</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-inetptonw">InetPton</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringexw">RtlIpv4AddressToStringEx</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4stringtoaddressa">RtlIpv4StringToAddress</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4stringtoaddressexw">RtlIpv4StringToAddressEx</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringa">RtlIpv6AddressToString</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringexw">RtlIpv6AddressToStringEx</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa">RtlIpv6StringToAddress</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6stringtoaddressexw">RtlIpv6StringToAddressEx</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_addr">inet_addr</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_ntoa">inet_ntoa</a>
