---
UID: NF:winsock2.WSAAddressToStringA
title: WSAAddressToStringA function
author: windows-sdk-content
description: Converts all components of a sockaddr structure into a human-readable string representation of the address.
old-location: winsock\wsaaddresstostring_2.htm
old-project: WinSock
ms.assetid: d72e55e6-79a9-4386-9e1a-24a322f13426
ms.author: windowssdkdev
ms.date: 04/30/2018
ms.keywords: WSAAddressToString, WSAAddressToString function [Winsock], WSAAddressToStringA, WSAAddressToStringW, _win32_wsaaddresstostring_2, winsock.wsaaddresstostring_2, winsock2/WSAAddressToString, winsock2/WSAAddressToStringA, winsock2/WSAAddressToStringW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winsock2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WSAAddressToStringW (Unicode) and WSAAddressToStringA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WSAECOMPARATOR, *PWSAECOMPARATOR, *LPWSAECOMPARATOR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ws2_32.dll
api_name:
-	WSAAddressToString
-	WSAAddressToStringA
-	WSAAddressToStringW
product: Windows
targetos: Windows
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSAAddressToStringA function


## -description



			The 
<b>WSAAddressToString</b> function converts all components of a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">sockaddr</a> structure into a human-readable string representation of the address.

This is intended to be used mainly for display purposes. If the caller requires that the translation to be performed by a particular provider, it should supply the corresponding 
<a href="https://msdn.microsoft.com/758c5553-056f-4ea5-a851-30ef641ffb14">WSAPROTOCOL_INFO</a> structure in the <i>lpProtocolInfo</i> parameter.


## -parameters




### -param lpsaAddress [in]

A pointer to the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">sockaddr</a> structure to translate into a string.


### -param dwAddressLength [in]

The length, in bytes, of the address in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">sockaddr</a> structure pointed to by the <i>lpsaAddress</i> parameter. The <i>dwAddressLength</i> parameter may vary in size with different protocols.


### -param lpProtocolInfo [in, optional]

A pointer to the 
<a href="https://msdn.microsoft.com/758c5553-056f-4ea5-a851-30ef641ffb14">WSAPROTOCOL_INFO</a> structure for a particular provider. If this is parameter is <b>NULL</b>, the call is routed to the provider of the first protocol supporting the address family indicated in the <i>lpsaAddress</i> parameter.


### -param lpszAddressString [in, out]

A pointer to the buffer that receives the human-readable address string.


### -param lpdwAddressStringLength [in, out]

On input, this parameter specifies the length of the buffer pointed to by the <i>lpszAddressString</i> parameter. The length is represented in bytes for ANSI strings, and in WCHARs for Unicode strings. On output, this parameter returns the length of the string including the <b>NULL</b> terminator actually copied into the buffer pointed to by the <i>lpszAddressString</i> parameter. If the specified buffer is not large enough, the function fails with a specific error of 
<a href="windows_sockets_error_codes_2.htm">WSAEFAULT</a> and this parameter is updated with the required size.


## -returns



If no error occurs, 
<b>WSAAddressToString</b> returns a value of zero. Otherwise, the value SOCKET_ERROR is returned, and a specific error number can be retrieved by calling 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The specified <i>lpcsAddress</i>, <i>lpProtocolInfo</i>, and <i>lpszAddressString</i> parameters point to memory that is not all in the address space of the process, or the buffer pointed to by the <i>lpszAddressString</i> parameter is too small. Pass in a larger buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed. This error is returned if the <i>lpsaAddress</i>, <i>dwAddressLength</i>, or <i>lpdwAddressStringLength</i> parameter are <b>NULL</b>. This error is also returned if the specified address is not a valid socket address, or no transport provider supports the indicated address family.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAENOBUFS</a></b></dt>
</dl>
</td>
<td width="60%">
No buffer space is available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSANOTINITIALISED</a></b></dt>
</dl>
</td>
<td width="60%">
The Winsock 2 DLL has not been initialized. The application must first call 
<a href="https://msdn.microsoft.com/08299592-867c-491d-9769-d16602133659">WSAStartup</a> before calling any Windows Sockets functions.

</td>
</tr>
</table>
 




## -remarks



The 
<b>WSAAddressToString</b> function provides a protocol-independent address-to-string translation. The 
<b>WSAAddressToString</b> function takes a socket address structure pointed to by the <i>lpsaAddress</i> parameter and returns a pointer to <b>NULL</b>-terminated string that represents the socket address in the <i>lpszAddressString</i> parameter. While the <a href="https://msdn.microsoft.com/01cd32e7-a01d-40e8-afb5-69223d643a0e">inet_ntoa</a> function works only with IPv4 addresses, the <b>WSAAddressToString</b> function works with any socket address supported by a Winsock provider on the local computer including IPv6 addresses.

If the <i>lpsaAddress</i> parameter points to an IPv4 socket address (the address family is  <b>AF_INET</b>), then the address string returned in the buffer pointed to by the <i>lpszAddressString</i> parameter is  in dotted-decimal notation as in "192.168.16.0", an example of an IPv4 address in dotted-decimal notation.   

If the <i>lpsaAddress</i> parameter points to an IPv6 socket address (the address family is  <b>AF_INET6</b>), then the address string returned in the buffer pointed to by the <i>lpszAddressString</i> parameter is  in Internet standard format. The basic string representation consists of 8 hexadecimal numbers separated by colons. A string of consecutive zero numbers is replaced with a double-colon. There can only be one double-colon in the string representation of the IPv6 address. 

If the length of the buffer pointed to by the <i>lpszAddressString</i> parameter is not large enough to receive the string representation of the socket address, <b>WSAAddressToString</b> returns 
								<a href="windows_sockets_error_codes_2.htm">WSAEFAULT</a>. 

Support for IPv6 addresses using the <b>WSAAddressToString</b> function was added on Windows XP with Service Pack 1 (SP1)
  and later. IPv6 must also be installed on the local computer for the <b>WSAAddressToString</b> function to support IPv6 addresses. 

<b>Windows Phone 8:</b> The <b>WSAAddressToStringW</b> function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: The <b>WSAAddressToStringW</b> function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.




## -see-also




<a href="https://msdn.microsoft.com/1e26b88c-808f-4807-8641-e5c6b10853ad">InetNtop</a>



<a href="https://msdn.microsoft.com/d0705997-0dc7-443b-a43f-611301cc9169">InetPton</a>



<a href="https://msdn.microsoft.com/f198b770-9429-4b51-9fb4-06cf9917bc21">RtlIpv4AddressToString</a>



<a href="https://msdn.microsoft.com/4244eaaf-8522-4edb-abb8-dc2b063c9076">RtlIpv4AddressToStringEx</a>



<a href="https://msdn.microsoft.com/79896c13-a671-423e-975e-98a4ccfa1eb8">RtlIpv4StringToAddress</a>



<a href="https://msdn.microsoft.com/72d20cf0-38ff-4c00-93ec-949aaf6f96e2">RtlIpv4StringToAddressEx</a>



<a href="https://msdn.microsoft.com/a891adb0-6c2d-4b69-a0de-4a615be938e3">RtlIpv6AddressToString</a>



<a href="https://msdn.microsoft.com/a7de2da3-21ea-42fa-9474-f33252838632">RtlIpv6AddressToStringEx</a>



<a href="https://msdn.microsoft.com/3cd3bfcf-e9b2-4ee6-8e93-a31a70fc3ad3">RtlIpv6StringToAddress</a>



<a href="https://msdn.microsoft.com/3a95c405-3f2c-4bd5-805e-3e879c4c20e2">RtlIpv6StringToAddressEx</a>



<a href="https://msdn.microsoft.com/758c5553-056f-4ea5-a851-30ef641ffb14">WSAPROTOCOL_INFO</a>



<a href="https://msdn.microsoft.com/08299592-867c-491d-9769-d16602133659">WSAStartup</a>



<a href="https://msdn.microsoft.com/7b9946c3-c8b3-45ae-9bde-03faaf604bba">WSAStringToAddress</a>



<a href="https://msdn.microsoft.com/7d6df658-9d83-45c7-97e7-b2a016a73847">inet_addr</a>



<a href="https://msdn.microsoft.com/01cd32e7-a01d-40e8-afb5-69223d643a0e">inet_ntoa</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">sockaddr</a>
 

 

