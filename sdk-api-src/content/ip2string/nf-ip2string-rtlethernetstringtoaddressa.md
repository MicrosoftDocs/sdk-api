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

# RtlEthernetStringToAddressA function


## -description


The 
<b>RtlEthernetStringToAddress</b> function  converts a string representation of an Ethernet MAC address to a binary format of the Ethernet address.



## -parameters




### -param S [in]

A pointer to a buffer containing the <b>NULL</b>-terminated string representation of the Ethernet MAC  address. 


### -param Terminator [out]

A parameter that receives a pointer to the character that terminated
        the converted string. This can be used by the caller to extract more information from the string.


### -param Addr [out]

A pointer where the binary representation of the Ethernet MAC address is to be stored.


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
An invalid parameter was passed to the function. This error is returned if the string pointed to by the <i>S</i> parameter did not contain a proper string representation of an Ethernet MAC address.

This error code is defined in the <i>Ntstatus.h</i> header file.

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
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>
 




## -remarks



The <b>RtlEthernetStringToAddress</b> function is used to convert a string representation of an Ethernet EUI-48 data-link layer address (also commonly known as a MAC address) to binary format of the Ethernet address. The string represents a numeric Ethernet address
    expressed in the non-DIX standard "-'' notation.  The value
    returned is a number suitable for use as an Ethernet address.  All
    Ethernet addresses are returned in network order (bytes ordered from
    left to right).


The string pointed to by the <i>S</i> parameter must be represented in the form for an Ethernet MAC address string in the non-DIX standard "-" notation. The basic string representation of an Ethernet MAC address consists of 6 pairs of hexadecimal numbers
    separated by dashes (F4-CE-46-2D-90-8C, for example). 

On success, the <i>Terminator</i> parameter points to the character that terminated the string that was converted. This allows an application to pass a string that contains an Ethernet address plus additional information to the <b>RtlEthernetStringToAddress</b> function and then parse the remaining information. 

<b>RtlEthernetStringToAddress</b> is a convenience function that does not require that the Windows Sockets DLL be loaded to access a function provided in Windows Sockets to perform string to Ethernet address conversion. 

When either UNICODE or _UNICODE is defined, <b>RtlEthernetStringToAddress</b> is defined to <b>RtlEthernetStringToAddressW</b>, the Unicode version of this function. The <i>S</i> and <i>Terminator</i> parameters are defined to the <b>PCWSTR</b> data type.





When both UNICODE and _UNICODE are not defined, <b>RtlEthernetStringToAddress</b> is defined to <b>RtlEthernetStringToAddressA</b>, the ANSI version of this function. The <i>S</i> and <i>Terminator</i> parameters are defined to the <b>PCSTR</b> data type.



The <b>DL_EUI48</b> data type is defined in the <i>Mstcpip.h</i>  header file.




## -see-also




<a href="https://msdn.microsoft.com/5DE1A1EF-86B3-4414-A21F-90635B48242A">RtlEthernetAddressToString</a>
 

 

