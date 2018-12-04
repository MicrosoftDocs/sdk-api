---
UID: NF:ip2string.RtlEthernetAddressToStringA
title: RtlEthernetAddressToStringA function
author: windows-sdk-content
description: Converts a binary Ethernet address to a string representation of the Ethernet MAC address.
old-location: iphlp\rtlethernetaddresstostring.htm
tech.root: IpHlp
ms.assetid: 5DE1A1EF-86B3-4414-A21F-90635B48242A
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: RtlEthernetAddressToString, RtlEthernetAddressToString function [IP Helper], RtlEthernetAddressToStringA, RtlEthernetAddressToStringW, ip2string/RtlEthernetAddressToString, ip2string/RtlEthernetAddressToStringA, ip2string/RtlEthernetAddressToStringW, iphlp.rtlethernetaddresstostring
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ip2string.h
req.include-header: Mstcpip.h, Ip2string.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RtlEthernetAddressToStringW (Unicode) and RtlEthernetAddressToStringA (ANSI)
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
 - RtlEthernetAddressToString
 - RtlEthernetAddressToStringA
 - RtlEthernetAddressToStringW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RtlEthernetAddressToStringA function


## -description


The 
<b>RtlEthernetAddressToString</b> function  converts a binary Ethernet address to a string representation of the Ethernet MAC address.



## -parameters




### -param Addr [in]

The Ethernet address in binary format. The Ethernet address is in network order (bytes ordered from
    left to right).



### -param S [out]

A pointer to a buffer in which to store the <b>NULL</b>-terminated string representation of the Ethernet address. This buffer should be large enough to hold at least 18 characters.


## -returns



A pointer to the NULL character inserted at the end of the string representation of the Ethernet MAC address.
This can be used by the caller to easily append more information to the string.




## -remarks



The <b>RtlEthernetAddressToString</b> function is used to convert a binary Ethernet address to the string representation of the Ethernet address in Ethernet EUI-48 data-link layer address format (also commonly known as a MAC address). The string represents a numeric Ethernet address
    expressed in the non-DIX standard "-'' notation.

The string returned in the <i>S</i> parameter is represented in the form for an Ethernet MAC address string in the non-DIX standard "-" notation. The basic string representation of an Ethernet MAC address consists of 6 pairs of hexadecimal numbers
    separated by dashes (F4-CE-46-2D-90-8C, for example). 

<b>RtlEthernetAddressToString</b> is a convenience function that does not require that the Windows Sockets DLL be loaded to access a function provided in Windows Sockets to perform string to Ethernet address conversion. 

When either UNICODE or _UNICODE is defined, <b>RtlEthernetAddressToString</b> is defined to <b>RtlEthernetAddressToStringW</b>, the Unicode version of this function. The string parameter <i>S</i> and the function return value are defined to the <b>PWSTR</b> data type.



When both UNICODE and _UNICODE are not defined, <b>RtlEthernetAddressToString</b> is defined to <b>RtlEthernetAddressToStringA</b>, the ANSI version of this function. The string parameter <i>S</i> and the function return value are defined to the <b>PSTR</b> data type.



The <b>DL_EUI48</b> data type is defined in the <i>Mstcpip.h</i>  header file.




## -see-also




<a href="https://msdn.microsoft.com/9FE1F2C6-971E-4789-9D30-4C129B3951F4">RtlEthernetStringToAddress</a>
 

 

