---
UID: NF:ip2string.RtlIpv4AddressToStringW
title: RtlIpv4AddressToStringW function
author: windows-sdk-content
description: Converts an IPv4 address to a string in Internet standard dotted-decimal format.
old-location: iphlp\rtlipv4addresstostring.htm
tech.root: IpHlp
ms.assetid: f198b770-9429-4b51-9fb4-06cf9917bc21
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RtlIpv4AddressToString, RtlIpv4AddressToString function [IP Helper], RtlIpv4AddressToStringA, RtlIpv4AddressToStringW, ip2string/RtlIpv4AddressToString, ip2string/RtlIpv4AddressToStringA, ip2string/RtlIpv4AddressToStringW, iphlp.rtlipv4addresstostring
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: 
req.dll: Ntdll.dll
req.irql: 
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RtlIpv4AddressToStringW function


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

An import library containing the <b>RtlIpv4AddressToString</b> function is not included in the Microsoft Windows Software Development Kit (SDK) released for Windows Vista. The <b>RtlIpv4AddressToString</b> function  is included in the <i>Ntdll.lib</i> import library included in the Windows Driver Kit (WDK). An application could also use the <a href="https://msdn.microsoft.com/29514410-89fe-4888-8b34-0c30d5af237f">GetModuleHandle</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to retrieve the function pointer from the <i>Ntdll.dll</i> and call this function.




## -see-also




<a href="https://msdn.microsoft.com/29514410-89fe-4888-8b34-0c30d5af237f">GetModuleHandle</a>



<a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a>



<a href="https://msdn.microsoft.com/1e26b88c-808f-4807-8641-e5c6b10853ad">InetNtop</a>



<a href="https://msdn.microsoft.com/d0705997-0dc7-443b-a43f-611301cc9169">InetPton</a>



<a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a>



<a href="https://msdn.microsoft.com/4244eaaf-8522-4edb-abb8-dc2b063c9076">RtlIpv4AddressToStringEx</a>



<a href="https://msdn.microsoft.com/79896c13-a671-423e-975e-98a4ccfa1eb8">RtlIpv4StringToAddress</a>



<a href="https://msdn.microsoft.com/72d20cf0-38ff-4c00-93ec-949aaf6f96e2">RtlIpv4StringToAddressEx</a>



<a href="https://msdn.microsoft.com/a891adb0-6c2d-4b69-a0de-4a615be938e3">RtlIpv6AddressToString</a>



<a href="https://msdn.microsoft.com/a7de2da3-21ea-42fa-9474-f33252838632">RtlIpv6AddressToStringEx</a>



<a href="https://msdn.microsoft.com/3cd3bfcf-e9b2-4ee6-8e93-a31a70fc3ad3">RtlIpv6StringToAddress</a>



<a href="https://msdn.microsoft.com/3a95c405-3f2c-4bd5-805e-3e879c4c20e2">RtlIpv6StringToAddressEx</a>



<a href="https://msdn.microsoft.com/7d6df658-9d83-45c7-97e7-b2a016a73847">inet_addr</a>



<a href="https://msdn.microsoft.com/01cd32e7-a01d-40e8-afb5-69223d643a0e">inet_ntoa</a>
 

 

