---
UID: NF:ip2string.RtlIpv6StringToAddressA
title: RtlIpv6StringToAddressA function (ip2string.h)
author: windows-sdk-content
description: Converts a string representation of an IPv6 address to a binary IPv6 address.
old-location: iphlp\rtlipv6stringtoaddress.htm
tech.root: IpHlp
ms.assetid: 3cd3bfcf-e9b2-4ee6-8e93-a31a70fc3ad3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RtlIpv6StringToAddress, RtlIpv6StringToAddress function [IP Helper], RtlIpv6StringToAddressA, RtlIpv6StringToAddressW, ip2string/RtlIpv6StringToAddress, ip2string/RtlIpv6StringToAddressA, ip2string/RtlIpv6StringToAddressW, iphlp.rtlipv6stringtoaddress
ms.topic: function
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
 - RtlIpv6StringToAddress
 - RtlIpv6StringToAddressA
 - RtlIpv6StringToAddressW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> to obtain the message string for the returned error.

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
    if the address is an IPv4-compatible address, an IPv4-mapped IPv6 address, or an ISATAP address. For more information, see section 5 of <a href="http://go.microsoft.com/fwlink/p/?linkid=222408">RFC 5942</a> published by the IETF. 

On success, the <i>Terminator</i> parameter points to the character that terminated the string that was converted. This allows an application to pass a string that contains and IP address plus additional information to the <b>RtlIpv6StringToAddress</b> function and then parse the remaining information. 

<div class="alert"><b>Note</b>  Some malformed IPv6 addresses (::::, for example) start with a valid IPv6 address.  The <b>RtlIpv6StringToAddress</b> function will return success, having parsed the valid part of the IPv6 address as the double colon (::).  The terminator then points to the third colon.  To validate that the entire passed-in string is a valid IPv6 address, you need to ensure that the terminator points to the correct character. If the  <i>S</i> parameter contains only an  IPv6 address, then the terminator should point to the <b>NULL</b> character at the end of the string.</div>
<div> </div>
When either UNICODE or _UNICODE is defined, <b>RtlIpv6StringToAddress</b> is defined to <b>RtlIpv6StringToAddressW</b>, the Unicode version of this function. The <i>S</i> and <i>Terminator</i> parameters are defined to the PCWSTR data type.





When both UNICODE and _UNICODE are not defined, <b>RtlIpv6StringToAddress</b> is defined to <b>RtlIpv6StringToAddressA</b>, the ANSI version of this function. The <i>S</i> and <i>Terminator</i> parameters are defined to the PCSTR data type.



The <a href="https://msdn.microsoft.com/2029db76-3fe1-4560-b753-910c48cbc578">IN6_ADDR</a> structure is defined in the In6addr.h header file.

An import library containing the <b>RtlIpv6StringToAddress</b> function is not included in the Microsoft Windows Software Development Kit (SDK) released for Windows Vista. The <b>RtlIpv6StringToAddress</b> function is included in the <i>Ntdll.lib</i> import library included in the Windows Driver Kit (WDK). An application could also use the <a href="https://msdn.microsoft.com/29514410-89fe-4888-8b34-0c30d5af237f">GetModuleHandle</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to retrieve the function pointer from the <i>Ntdll.dll</i> and call this function.




## -see-also




<a href="https://msdn.microsoft.com/29514410-89fe-4888-8b34-0c30d5af237f">GetModuleHandle</a>



<a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a>



<a href="https://msdn.microsoft.com/2029db76-3fe1-4560-b753-910c48cbc578">IN6_ADDR</a>



<a href="https://msdn.microsoft.com/1e26b88c-808f-4807-8641-e5c6b10853ad">InetNtop</a>



<a href="https://msdn.microsoft.com/d0705997-0dc7-443b-a43f-611301cc9169">InetPton</a>



<a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a>



<a href="https://msdn.microsoft.com/f198b770-9429-4b51-9fb4-06cf9917bc21">RtlIpv4AddressToString</a>



<a href="https://msdn.microsoft.com/4244eaaf-8522-4edb-abb8-dc2b063c9076">RtlIpv4AddressToStringEx</a>



<a href="https://msdn.microsoft.com/79896c13-a671-423e-975e-98a4ccfa1eb8">RtlIpv4StringToAddress</a>



<a href="https://msdn.microsoft.com/72d20cf0-38ff-4c00-93ec-949aaf6f96e2">RtlIpv4StringToAddressEx</a>



<a href="https://msdn.microsoft.com/a891adb0-6c2d-4b69-a0de-4a615be938e3">RtlIpv6AddressToString</a>



<a href="https://msdn.microsoft.com/a7de2da3-21ea-42fa-9474-f33252838632">RtlIpv6AddressToStringEx</a>



<a href="https://msdn.microsoft.com/3a95c405-3f2c-4bd5-805e-3e879c4c20e2">RtlIpv6StringToAddressEx</a>



<a href="https://msdn.microsoft.com/7d6df658-9d83-45c7-97e7-b2a016a73847">inet_addr</a>



<a href="https://msdn.microsoft.com/01cd32e7-a01d-40e8-afb5-69223d643a0e">inet_ntoa</a>
 

 

