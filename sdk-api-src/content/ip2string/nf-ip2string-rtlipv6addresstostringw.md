---
UID: NF:ip2string.RtlIpv6AddressToStringW
title: RtlIpv6AddressToStringW function
author: windows-sdk-content
description: Converts an IPv6 address to a string in Internet standard format.
old-location: iphlp\rtlipv6addresstostring.htm
old-project: iphlp
ms.assetid: a891adb0-6c2d-4b69-a0de-4a615be938e3
ms.author: windowssdkdev
ms.date: 08/15/2018
ms.keywords: RtlIpv6AddressToString, RtlIpv6AddressToString function [IP Helper], RtlIpv6AddressToStringA, RtlIpv6AddressToStringW, ip2string/RtlIpv6AddressToString, ip2string/RtlIpv6AddressToStringA, ip2string/RtlIpv6AddressToStringW, iphlp.rtlipv6addresstostring
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ip2string.h
req.include-header: Mstcpip.h, Ip2string.h
req.redist: 
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
tech.root: 
req.typenames: URLASSOCIATIONDIALOG_IN_FLAGS
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
product: Windows
targetos: Windows
req.lib: 
req.dll: Ntdll.dll
req.irql: 
req.product: GDI+ 1.1
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
    if the address is an IPv4-compatible address, an IPv4-mapped IPv6 address, or an ISATAP address. For more information, see section 5 of <a href="http://go.microsoft.com/fwlink/p/?linkid=222408">RFC 5942</a> published by the IETF. 

<b>RtlIpv6AddressToString</b> is a convenience function that does not require that the Windows Sockets DLL be loaded to access a function provided in Windows Sockets to perform IP address to string conversion. 

When either UNICODE or _UNICODE is defined, <b>RtlIpv6AddressToString</b> is defined to <b>RtlIpv6AddressToStringW</b>, the Unicode version of this function. The string parameter <i>S</i> and the function return value are defined to the PWSTR data type.



When both UNICODE and _UNICODE are not defined, <b>RtlIpv6AddressToString</b> is defined to <b>RtlIpv6AddressToStringA</b>, the ANSI version of this function. The string parameter <i>S</i> and the function return value are defined to the PSTR data type.



The <b>IN6_ADDR</b> structure is defined in the <i>In6addr.h</i> header file.

An import library containing the <b>RtlIpv6AddressToString</b> function is not included in the Microsoft Windows Software Development Kit (SDK) released for Windows Vista. The <b>RtlIpv6AddressToString</b> function is included in the <i>Ntdll.lib</i> import library included in the Windows Driver Kit (WDK). An application could also use the <a href="https://msdn.microsoft.com/29514410-89fe-4888-8b34-0c30d5af237f">GetModuleHandle</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to retrieve the function pointer from the <i>Ntdll.dll</i> and call this function.




## -see-also




<a href="https://msdn.microsoft.com/29514410-89fe-4888-8b34-0c30d5af237f">GetModuleHandle</a>



<a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a>



<a href="https://msdn.microsoft.com/1e26b88c-808f-4807-8641-e5c6b10853ad">InetNtop</a>



<a href="https://msdn.microsoft.com/d0705997-0dc7-443b-a43f-611301cc9169">InetPton</a>



<a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a>



<a href="https://msdn.microsoft.com/f198b770-9429-4b51-9fb4-06cf9917bc21">RtlIpv4AddressToString</a>



<a href="https://msdn.microsoft.com/4244eaaf-8522-4edb-abb8-dc2b063c9076">RtlIpv4AddressToStringEx</a>



<a href="https://msdn.microsoft.com/79896c13-a671-423e-975e-98a4ccfa1eb8">RtlIpv4StringToAddress</a>



<a href="https://msdn.microsoft.com/72d20cf0-38ff-4c00-93ec-949aaf6f96e2">RtlIpv4StringToAddressEx</a>



<a href="https://msdn.microsoft.com/a7de2da3-21ea-42fa-9474-f33252838632">RtlIpv6AddressToStringEx</a>



<a href="https://msdn.microsoft.com/3cd3bfcf-e9b2-4ee6-8e93-a31a70fc3ad3">RtlIpv6StringToAddress</a>



<a href="https://msdn.microsoft.com/3a95c405-3f2c-4bd5-805e-3e879c4c20e2">RtlIpv6StringToAddressEx</a>



<a href="https://msdn.microsoft.com/7d6df658-9d83-45c7-97e7-b2a016a73847">inet_addr</a>



<a href="https://msdn.microsoft.com/01cd32e7-a01d-40e8-afb5-69223d643a0e">inet_ntoa</a>
 

 

