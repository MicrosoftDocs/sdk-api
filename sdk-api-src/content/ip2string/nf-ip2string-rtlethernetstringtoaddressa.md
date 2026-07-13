---
UID: NF:ip2string.RtlEthernetStringToAddressA
title: RtlEthernetStringToAddressA function (ip2string.h)
description: Converts a string representation of an Ethernet MAC address to a binary format of the Ethernet address. (ANSI)
helpviewer_keywords: ["RtlEthernetStringToAddressA", "ip2string/RtlEthernetStringToAddressA"]
old-location: iphlp\rtlethernetstringtoaddress.htm
tech.root: IpHlp
ms.assetid: 9FE1F2C6-971E-4789-9D30-4C129B3951F4
ms.date: 12/05/2018
ms.keywords: RtlEthernetStringToAddress, RtlEthernetStringToAddress function [IP Helper], RtlEthernetStringToAddressA, RtlEthernetStringToAddressW, ip2string/RtlEthernetStringToAddress, ip2string/RtlEthernetStringToAddressA, ip2string/RtlEthernetStringToAddressW, iphlp.rtlethernetstringtoaddress
req.header: ip2string.h
req.include-header: Mstcpip.h, Ip2string.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RtlEthernetStringToAddressW (Unicode) and RtlEthernetStringToAddressA (ANSI)
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
 - RtlEthernetStringToAddressA
 - ip2string/RtlEthernetStringToAddressA
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
 - RtlEthernetStringToAddress
 - RtlEthernetStringToAddressA
 - RtlEthernetStringToAddressW
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
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to obtain the message string for the returned error.

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





> [!NOTE]
> The ip2string.h header defines RtlEthernetStringToAddress as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlethernetaddresstostringa">RtlEthernetAddressToString</a>
