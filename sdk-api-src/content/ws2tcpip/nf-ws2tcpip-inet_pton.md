---
UID: NF:ws2tcpip.inet_pton
title: inet_pton function
author: windows-sdk-content
description: The InetPton function converts an IPv4 or IPv6 Internet network address in its standard text presentation form into its numeric binary form. The ANSI version of this function is inet_pton.
old-location: winsock\inet_pton.htm
old-project: winsock
ms.assetid: d0705997-0dc7-443b-a43f-611301cc9169
ms.author: windowssdkdev
ms.date: 07/10/2018
ms.keywords: AF_INET, AF_INET6, InetPton, InetPton function [Winsock], InetPtonA, InetPtonA or inet_pton, InetPtonW, inet_pton, winsock.inet_pton, ws2tcpip/InetPton, ws2tcpip/InetPtonA or inet_pton, ws2tcpip/InetPtonW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ws2tcpip.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: InetPtonW (Unicode) and InetPtonA or inet_pton (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSPUPCALLTABLE, *LPWSPUPCALLTABLE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - InetPton
 - InetPtonA or inet_pton
 - InetPtonW
product: Windows
targetos: Windows
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# inet_pton function


## -description



			The 
<b>InetPton</b> function converts an IPv4 or IPv6 Internet network address in its standard text   presentation form into its numeric binary form. The ANSI version of this function is   <b>inet_pton</b>.


## -parameters




### -param Family [in]

The address family. 

Possible values for the address family are defined in the <i>Ws2def.h</i> header file. Note that the <i>Ws2def.h</i> header file is automatically included in <i>Winsock2.h</i>, and should never be used directly. Note that the values for the AF_ address family and PF_ protocol family constants  are identical (for example, <b>AF_INET</b> and <b>PF_INET</b>), so either constant can be used.

The values currently supported are <b>AF_INET</b> and <b>AF_INET6</b>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AF_INET"></a><a id="af_inet"></a><dl>
<dt><b>AF_INET</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The Internet Protocol version 4 (IPv4) address family. When this parameter is specified,  the <i>pszAddrString</i> parameter must point to a text representation of an IPv4 address and the <i>pAddrBuf</i> parameter  returns a pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff556972">IN_ADDR</a> structure that represents the IPv4 address. 

</td>
</tr>
<tr>
<td width="40%"><a id="AF_INET6"></a><a id="af_inet6"></a><dl>
<dt><b>AF_INET6</b></dt>
<dt>23</dt>
</dl>
</td>
<td width="60%">
The Internet Protocol version 6 (IPv6) address family. When this parameter is specified,  the <i>pszAddrString</i> parameter must point to a text representation of an IPv6 address and the <i>pAddrBuf</i> parameter  returns a pointer to an  <a href="https://msdn.microsoft.com/library/windows/hardware/ff554787">IN6_ADDR</a> structure that represents the IPv6 address.  

</td>
</tr>
</table>
 


### -param pszAddrString [in]

A pointer to the <b>NULL</b>-terminated string that contains the text representation of the IP address to convert to numeric binary form.

When the <i>Family</i> parameter is <b>AF_INET</b>, then the <i>pszAddrString</i> parameter must point to a text representation of an IPv4 address in standard dotted-decimal notation.

When the <i>Family</i> parameter is <b>AF_INET6</b>, then the <i>pszAddrString</i> parameter must point to a text representation of an IPv6 address in standard notation. 


### -param pAddrBuf [out]

A pointer to a buffer in which to store the numeric binary representation of the IP address. The IP address is returned in network byte order.

When the <i>Family</i> parameter is <b>AF_INET</b>, this buffer should be large enough to hold an <a href="https://msdn.microsoft.com/library/windows/hardware/ff556972">IN_ADDR</a> structure.

When the <i>Family</i> parameter is <b>AF_INET6</b>,  this buffer should be large enough to hold an <a href="https://msdn.microsoft.com/library/windows/hardware/ff554787">IN6_ADDR</a> structure.


## -returns



If no error occurs, 
the <b>InetPton</b> function returns a value of 1 and the buffer pointed to by the <i>pAddrBuf</i> parameter contains the binary numeric IP address in network byte order.

The <b>InetPton</b> function returns a value of 0 if the <i>pAddrBuf</i> parameter points to a string that is not a valid IPv4 dotted-decimal string or a valid IPv6 address string. Otherwise, a value of -1 is returned, and a specific error code can be retrieved by calling the  
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a> for extended error information.

If the function has an error, the extended error code returned by <a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a> can be one of the following values.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAEAFNOSUPPORT</a></b></dt>
</dl>
</td>
<td width="60%">
The address family specified in the <i>Family</i> parameter is not supported. This error is returned if the <i>Family</i> parameter specified was not <b>AF_INET</b> or <b>AF_INET6</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>pszAddrString</i> or <i>pAddrBuf</i> parameters are <b>NULL</b> or are not part of the user address space.

</td>
</tr>
</table>
 




## -remarks



The 
<b>InetPton</b> function is supported on Windows Vista
  and later.

The 
<b>InetPton</b> function provides a protocol-independent conversion of an Internet network address in its standard text   presentation form into its numeric binary form. The 
<b>InetPton</b> function takes a text representation of an Internet address pointed to  by the <i>pszAddrString</i> parameter and returns a pointer to the numeric binary IP address in the <i>pAddrBuf</i> parameter. While the <a href="https://msdn.microsoft.com/7d6df658-9d83-45c7-97e7-b2a016a73847">inet_addr</a>
		 function works only with IPv4 address strings, the <b>InetPton</b> function works with either IPv4 or IPv6 address strings.

The ANSI version of this function is <b>inet_pton</b> as defined in RFC 2553. For more information, see RFC 2553 available at the <a href="http://go.microsoft.com/fwlink/p/?linkid=86448">IETF website</a>.

The 
<b>InetPton</b> function does not require that the Windows Sockets DLL be loaded to perform conversion of a text string that represents an IP address to a numeric binary IP address.

If the <i>Family</i> parameter specified is <b>AF_INET</b>, then the <i>pszAddrString</i> parameter must point a text string of an IPv4 address  in dotted-decimal notation as in "192.168.16.0", an example of an IPv4 address in dotted-decimal notation.

If the <i>Family</i> parameter specified is <b>AF_INET6</b>, then the <i>pszAddrString</i> parameter must point a text string of an IPv6 address in Internet standard format. The basic string representation consists of 8 hexadecimal numbers separated by colons. A string of consecutive zero numbers may be replaced with a double-colon. There can only be one double-colon in the string representation of the IPv6 address. The last 32 bits may be represented in IPv4-style dotted-octet notation if the address is a IPv4-compatible address.

When UNICODE or _UNICODE is defined, <b>InetPton</b> is defined to <b>InetPtonW</b>, the Unicode version of this function. The <i>pszAddrString</i> parameter is defined to the <b>PCWSTR</b> data type.

When UNICODE or _UNICODE is not defined, <b>InetPton</b> is defined to <b>InetPtonA</b>, the ANSI version of this function. The ANSI version of this function is always defined as <a href="https://msdn.microsoft.com/1e26b88c-808f-4807-8641-e5c6b10853ad">inet_pton</a>. The <i>pszAddrString</i> parameter is defined to the <b>PCSTR</b> data type.

The <a href="https://msdn.microsoft.com/library/windows/hardware/ff556972">IN_ADDR</a> structure is defined in the <i>Inaddr.h</i> header file.

The <a href="https://msdn.microsoft.com/library/windows/hardware/ff554787">IN6_ADDR</a> structure is defined in the <i>In6addr.h</i> header file.

On Windows Vista and later, the <a href="https://msdn.microsoft.com/79896c13-a671-423e-975e-98a4ccfa1eb8">RtlIpv4StringToAddress</a> and <a href="https://msdn.microsoft.com/72d20cf0-38ff-4c00-93ec-949aaf6f96e2">RtlIpv4StringToAddressEx</a> functions can be used to convert a text representation of an IPv4 address in Internet standard dotted-decimal notation to a numeric binary address represented as an  <a href="https://msdn.microsoft.com/library/windows/hardware/ff556972">IN_ADDR</a> structure. On Windows Vista and later, the <a href="https://msdn.microsoft.com/3cd3bfcf-e9b2-4ee6-8e93-a31a70fc3ad3">RtlIpv6StringToAddress</a> and <a href="https://msdn.microsoft.com/3a95c405-3f2c-4bd5-805e-3e879c4c20e2">RtlIpv6StringToAddressEx</a> functions can be used to convert a string representation of an IPv6 address to a numeric binary IPv6 address represented as an <a href="https://msdn.microsoft.com/library/windows/hardware/ff554787">IN6_ADDR</a> structure. The <b>RtlIpv6StringToAddressEx</b> function is more flexible since it also converts a string representation of an IPv6 address that can include a scope ID and port in standard notation to a numeric binary form.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: The  <b>InetPtonW</b> function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff554787">IN6_ADDR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556972">IN_ADDR</a>



<a href="https://msdn.microsoft.com/1e26b88c-808f-4807-8641-e5c6b10853ad">InetNtop</a>



<a href="https://msdn.microsoft.com/f198b770-9429-4b51-9fb4-06cf9917bc21">RtlIpv4AddressToString</a>



<a href="https://msdn.microsoft.com/4244eaaf-8522-4edb-abb8-dc2b063c9076">RtlIpv4AddressToStringEx</a>



<a href="https://msdn.microsoft.com/79896c13-a671-423e-975e-98a4ccfa1eb8">RtlIpv4StringToAddress</a>



<a href="https://msdn.microsoft.com/72d20cf0-38ff-4c00-93ec-949aaf6f96e2">RtlIpv4StringToAddressEx</a>



<a href="https://msdn.microsoft.com/a891adb0-6c2d-4b69-a0de-4a615be938e3">RtlIpv6AddressToString</a>



<a href="https://msdn.microsoft.com/a7de2da3-21ea-42fa-9474-f33252838632">RtlIpv6AddressToStringEx</a>



<a href="https://msdn.microsoft.com/3cd3bfcf-e9b2-4ee6-8e93-a31a70fc3ad3">RtlIpv6StringToAddress</a>



<a href="https://msdn.microsoft.com/3a95c405-3f2c-4bd5-805e-3e879c4c20e2">RtlIpv6StringToAddressEx</a>



<a href="https://msdn.microsoft.com/7d6df658-9d83-45c7-97e7-b2a016a73847">inet_addr</a>



<a href="https://msdn.microsoft.com/01cd32e7-a01d-40e8-afb5-69223d643a0e">inet_ntoa</a>
 

 

