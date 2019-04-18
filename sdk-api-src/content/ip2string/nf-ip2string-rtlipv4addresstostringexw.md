---
UID: NF:ip2string.RtlIpv4AddressToStringExW
title: RtlIpv4AddressToStringExW function (ip2string.h)
author: windows-sdk-content
description: Converts an IPv4 address and port number to a string in Internet standard format.
old-location: iphlp\rtlipv4addresstostringex.htm
tech.root: IpHlp
ms.assetid: 4244eaaf-8522-4edb-abb8-dc2b063c9076
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RtlIpv4AddressToStringEx, RtlIpv4AddressToStringEx function [IP Helper], RtlIpv4AddressToStringExW, ip2string/RtlIpv4AddressToStringEx, ip2string/RtlIpv4AddressToStringExW, iphlp.rtlipv4addresstostringex
ms.topic: function
req.header: ip2string.h
req.include-header: Mstcpip.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RtlIpv4AddressToStringExW (Unicode) and RtlIpv4AddressToStringEx (ANSI)
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
 - RtlIpv4AddressToStringEx
 - RtlIpv4AddressToStringEx
 - RtlIpv4AddressToStringExW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RtlIpv4AddressToStringExW function


## -description


The 
<b>RtlIpv4AddressToStringEx</b> function  converts an IPv4 address and port number to a string in Internet standard format.



## -parameters




### -param Address [in]

The IPv4 address in network byte order.


### -param Port [in]

The port number in network byte order format. This parameter is optional.


### -param AddressString [out]

A pointer to the buffer to receive the <b>NULL</b>-terminated string representation of the IPv4 address and port. This buffer should be large enough to hold at least INET_ADDRSTRLEN characters. The INET_ADDRSTRLEN value is defined in the <i>Ws2ipdef.h</i> header file.


### -param AddressStringLength [in, out]

On input, the number of characters that fit in the buffer pointed to by the <i>AddressString</i> parameter, including the NULL terminator.
        On output, this parameter contains the number of characters actually written
        to the buffer pointed to by the <i>AddressString</i> parameter.
        


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
An invalid parameter was passed to the function. This error is returned if a <b>NULL</b> pointer is passed in the <i>AddressString</i> or <i>AddressStringLength</i> parameter. This error is also returned if the length of the buffer pointed to by the <i>AddressString</i> parameter is not large enough to receive the string representation of the IPv4 address and port. 

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



The <b>RtlIpv4AddressToStringEx</b> function is used to convert an IPv4 address and port number to the string representation of the IPv4 address in Internet dotted-decimal format followed by a colon character and a string representation of the port. 

<b>RtlIpv4AddressToStringEx</b> is a convenience function that does not require that the Windows Sockets DLL be loaded to access a function provided in Windows Sockets to perform IP address to string conversion. 

If the length of the buffer pointed to by the <i>AddressString</i> parameter is not large enough to receive the string representation of the IPv4 address and port, <b>RtlIpv4AddressToStringEx</b> returns <b>ERROR_INVALID_PARAMETER</b> and sets the <i>AddressStringLength</i> parameter to the buffer length required. 

When either UNICODE or _UNICODE is defined, <b>RtlIpv4AddressToStringEx</b> is defined to <b>RtlIpv4AddressToStringExW</b>, the Unicode version of this function. The <i>AddressString</i> parameter is defined to the PWSTR data type.



When both UNICODE and _UNICODE are not defined, <b>RtlIpv4AddressToStringEx</b> is defined to <b>RtlIpv4AddressToStringExA</b>, the ANSI version of this function. The <i>AddressString</i> parameter is defined to the PSTR data type.



The <b>IN_ADDR</b> structure is defined in the <i>Inaddr.h</i> header file.

An import library containing the <b>RtlIpv4AddressToStringEx</b> function is not included in the Microsoft Windows Software Development Kit (SDK) released for Windows Vista. The <b>RtlIpv4AddressToStringEx</b> function is included in the <i>Ntdll.lib</i> import library included in the Windows Driver Kit (WDK). An application could also use the <a href="https://msdn.microsoft.com/29514410-89fe-4888-8b34-0c30d5af237f">GetModuleHandle</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to retrieve the function pointer from the <i>Ntdll.dll</i> and call this function.




## -see-also




<a href="https://msdn.microsoft.com/29514410-89fe-4888-8b34-0c30d5af237f">GetModuleHandle</a>



<a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a>



<a href="https://msdn.microsoft.com/1e26b88c-808f-4807-8641-e5c6b10853ad">InetNtop</a>



<a href="https://msdn.microsoft.com/d0705997-0dc7-443b-a43f-611301cc9169">InetPton</a>



<a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a>



<a href="https://msdn.microsoft.com/f198b770-9429-4b51-9fb4-06cf9917bc21">RtlIpv4AddressToString</a>



<a href="https://msdn.microsoft.com/79896c13-a671-423e-975e-98a4ccfa1eb8">RtlIpv4StringToAddress</a>



<a href="https://msdn.microsoft.com/72d20cf0-38ff-4c00-93ec-949aaf6f96e2">RtlIpv4StringToAddressEx</a>



<a href="https://msdn.microsoft.com/a891adb0-6c2d-4b69-a0de-4a615be938e3">RtlIpv6AddressToString</a>



<a href="https://msdn.microsoft.com/a7de2da3-21ea-42fa-9474-f33252838632">RtlIpv6AddressToStringEx</a>



<a href="https://msdn.microsoft.com/3cd3bfcf-e9b2-4ee6-8e93-a31a70fc3ad3">RtlIpv6StringToAddress</a>



<a href="https://msdn.microsoft.com/3a95c405-3f2c-4bd5-805e-3e879c4c20e2">RtlIpv6StringToAddressEx</a>



<a href="https://msdn.microsoft.com/7d6df658-9d83-45c7-97e7-b2a016a73847">inet_addr</a>



<a href="https://msdn.microsoft.com/01cd32e7-a01d-40e8-afb5-69223d643a0e">inet_ntoa</a>
 

 

