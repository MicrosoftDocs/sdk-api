---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

