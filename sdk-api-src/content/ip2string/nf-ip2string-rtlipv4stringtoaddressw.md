---
UID: NF:ip2string.RtlIpv4StringToAddressW
title: RtlIpv4StringToAddressW function (ip2string.h)
author: windows-sdk-content
description: Converts a string representation of an IPv4 address to a binary IPv4 address.
old-location: iphlp\rtlipv4stringtoaddress.htm
tech.root: IpHlp
ms.assetid: 79896c13-a671-423e-975e-98a4ccfa1eb8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RtlIpv4StringToAddress, RtlIpv4StringToAddress function [IP Helper], RtlIpv4StringToAddressA, RtlIpv4StringToAddressW, ip2string/RtlIpv4StringToAddress, ip2string/RtlIpv4StringToAddressA, ip2string/RtlIpv4StringToAddressW, iphlp.rtlipv4stringtoaddress
ms.topic: function
req.header: ip2string.h
req.include-header: Mstcpip.h, Ip2string.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RtlIpv4StringToAddressW (Unicode) and RtlIpv4StringToAddressA (ANSI)
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
 - RtlIpv4StringToAddress
 - RtlIpv4StringToAddressA
 - RtlIpv4StringToAddressW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RtlIpv4StringToAddressW function


## -description


The 
<b>RtlIpv4StringToAddress</b> function  converts a string representation of an IPv4 address to a binary IPv4 address.



## -parameters




### -param S [in]

A pointer to a buffer containing the <b>NULL</b>-terminated string representation of the IPv4 address. 


### -param Strict [in]

A value that indicates whether the string must be an IPv4 address represented in strict four-part dotted-decimal notation.  If this parameter is <b>TRUE</b>, the string must be dotted-decimal with four parts.
             If this parameter is <b>FALSE</b>, any of four possible forms are allowed, with decimal,
             octal, or hexadecimal notation. See the Remarks section for details.


### -param Terminator [out]

A parameter that receives a pointer to the character that terminated
        the converted string. This can be used by the caller to extract more information from the string.


### -param Addr [out]

A pointer where the binary representation of the IPv4 address is to be stored.


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
An invalid parameter was passed to the function. This error is returned if the <i>Strict</i> parameter was set to <b>TRUE</b>, but the string pointed to by the <i>S</i> parameter did not contain a four-part dotted decimal string representation of an IPv4 address. This error is also returned if the string pointed to by the <i>S</i> parameter did not contain a proper string representation of an IPv4 address.

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



The <b>RtlIpv4StringToAddress</b> function is used to convert a string representation of the IPv4 address to an IPv4 address returned in network order (bytes ordered from
    left to right). 

<b>RtlIpv4StringToAddress</b> is a convenience function that does not require that the Windows Sockets DLL be loaded to access a function provided in Windows Sockets to perform string to IP address conversion. 

If the <i>Strict</i> parameter is set to <b>TRUE</b>, then the string pointed to by the <i>S</i> parameter must be in strict dotted-decimal notation. This strict format requires that four parts are specified. Each part is interpreted as a decimal byte of data
    and assigned, from left to right, to the four bytes of an IPv4
    address.   

When the <i>Strict</i> parameter is set to <b>FALSE</b>, the string pointed to by <i>S</i> parameter may be in any of the several possible formats. When the buffer pointed to by <i>S</i> parameter contains a three-part address string, the last part is interpreted
    as a 16-bit quantity and placed in the right most two bytes of the
    network address.  This makes the three-part address format
    convenient for specifying Class B network addresses as
    "128.net.host". When the buffer pointed to by <i>S</i> parameter contains a two-part address string, the last part is interpreted
    as a 24-bit quantity and placed in the right most three bytes of the
    network address.  This makes the two part address format convenient
    for specifying Class A network addresses as "net.host". When the buffer pointed to by <i>S</i> parameter contains only a one-part address string, the value is stored directly in the
    network address without any byte rearrangement.


 

On success, the <i>Terminator</i> parameter points to the character that terminated the string that was converted. This allows an application to pass a string that contains an IP address plus additional information to the <b>RtlIpv4StringToAddress</b> function and then parse the remaining information. 

When either UNICODE or _UNICODE is defined, <b>RtlIpv4StringToAddress</b> is defined to <b>RtlIpv4StringToAddressW</b>, the Unicode version of this function. The <i>S</i> parameter is defined to the PCWSTR data type and the <i>Terminator</i> parameter is defined to the LPCWSTR data type.



When both UNICODE and _UNICODE are not defined, <b>RtlIpv4StringToAddress</b> is defined to <b>RtlIpv4StringToAddressA</b>, the ANSI version of this function. The <i>S</i> and <i>Terminator</i> parameters are defined to the PCSTR data type.



The <a href="https://msdn.microsoft.com/fc41a2d1-ea6e-41bb-b2c8-531ac8b5434c">IN_ADDR</a> structure is defined in the <i>Inaddr.h</i> header file.

An import library containing the <b>RtlIpv4StringToAddress</b> function is not included in the Microsoft Windows Software Development Kit (SDK) released for Windows Vista. The <b>RtlIpv4StringToAddress</b> function is included in the <i>Ntdll.lib</i> import library included in the Windows Driver Kit (WDK). An application could also use the <a href="https://msdn.microsoft.com/29514410-89fe-4888-8b34-0c30d5af237f">GetModuleHandle</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to retrieve the function pointer from the <i>Ntdll.dll</i> and call this function.




## -see-also




<a href="https://msdn.microsoft.com/29514410-89fe-4888-8b34-0c30d5af237f">GetModuleHandle</a>



<a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a>



<a href="https://msdn.microsoft.com/1e26b88c-808f-4807-8641-e5c6b10853ad">InetNtop</a>



<a href="https://msdn.microsoft.com/d0705997-0dc7-443b-a43f-611301cc9169">InetPton</a>



<a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a>



<a href="https://msdn.microsoft.com/f198b770-9429-4b51-9fb4-06cf9917bc21">RtlIpv4AddressToString</a>



<a href="https://msdn.microsoft.com/4244eaaf-8522-4edb-abb8-dc2b063c9076">RtlIpv4AddressToStringEx</a>



<a href="https://msdn.microsoft.com/72d20cf0-38ff-4c00-93ec-949aaf6f96e2">RtlIpv4StringToAddressEx</a>



<a href="https://msdn.microsoft.com/a891adb0-6c2d-4b69-a0de-4a615be938e3">RtlIpv6AddressToString</a>



<a href="https://msdn.microsoft.com/a7de2da3-21ea-42fa-9474-f33252838632">RtlIpv6AddressToStringEx</a>



<a href="https://msdn.microsoft.com/3cd3bfcf-e9b2-4ee6-8e93-a31a70fc3ad3">RtlIpv6StringToAddress</a>



<a href="https://msdn.microsoft.com/3a95c405-3f2c-4bd5-805e-3e879c4c20e2">RtlIpv6StringToAddressEx</a>



<a href="https://msdn.microsoft.com/7d6df658-9d83-45c7-97e7-b2a016a73847">inet_addr</a>



<a href="https://msdn.microsoft.com/01cd32e7-a01d-40e8-afb5-69223d643a0e">inet_ntoa</a>
 

 

