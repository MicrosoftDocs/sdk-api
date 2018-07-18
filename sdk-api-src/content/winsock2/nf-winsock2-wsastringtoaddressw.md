---
UID: NF:winsock2.WSAStringToAddressW
title: WSAStringToAddressW function
author: windows-sdk-content
description: The WSAStringToAddress function converts a network address in its standard text presentation form into its numeric binary form in a sockaddr structure, suitable for passing to Windows Sockets routines that take such a structure.
old-location: winsock\wsastringtoaddress_2.htm
old-project: winsock
ms.assetid: 7b9946c3-c8b3-45ae-9bde-03faaf604bba
ms.author: windowssdkdev
ms.date: 07/10/2018
ms.keywords: WSAStringToAddress, WSAStringToAddress function [Winsock], WSAStringToAddressA, WSAStringToAddressW, _win32_wsastringtoaddress_2, winsock.wsastringtoaddress_2, winsock2/WSAStringToAddress, winsock2/WSAStringToAddressA, winsock2/WSAStringToAddressW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winsock2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WSAStringToAddressW (Unicode) and WSAStringToAddressA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSAECOMPARATOR, *PWSAECOMPARATOR, *LPWSAECOMPARATOR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - WSAStringToAddress
 - WSAStringToAddressA
 - WSAStringToAddressW
product: Windows
targetos: Windows
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSAStringToAddressW function


## -description


The 
<b>WSAStringToAddress</b> function converts a network address in its standard text   presentation form into its numeric binary form in a <a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">sockaddr</a> structure, suitable for passing to Windows Sockets routines that take such a structure.


## -parameters




### -param AddressString [in]

A pointer to the zero-terminated string that contains the network address in standard text form to convert.


### -param AddressFamily [in]

The address family of the network address pointed to by the <i>AddressString</i> parameter.


### -param lpProtocolInfo [in, optional]

The 
<a href="https://msdn.microsoft.com/758c5553-056f-4ea5-a851-30ef641ffb14">WSAPROTOCOL_INFO</a> structure associated with the provider to be used. If this is <b>NULL</b>, the call is routed to the provider of the first protocol supporting the indicated <i>AddressFamily</i>.


### -param lpAddress [out]

A pointer to a buffer that is filled with a  <a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">sockaddr</a> structure for the address string if the function succeeds.


### -param lpAddressLength [in, out]

A pointer to the length, in bytes, of the buffer pointed to by the <i>lpAddress</i> parameter. If the function call is successful, this parameter returns a pointer to the size of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">sockaddr</a> structure returned in the <i>lpAddress</i> parameter. If the specified buffer is not large enough, the function fails with a specific error of 
<a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAEFAULT</a> and this parameter is updated with the required size in bytes.


## -returns



The return value for 
<b>WSAStringToAddress</b> is zero if the operation was successful. Otherwise, the value SOCKET_ERROR is returned, and a specific error number can be retrieved by calling 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by the <i>lpAddress</i> parameter is too small. Pass in a larger buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
The functions was unable to translate the string into a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">sockaddr</a>. See the following Remarks section for more information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSANOTINITIALISED</a></b></dt>
</dl>
</td>
<td width="60%">
The WS2_32.DLL has not been initialized. The application must first call 
<a href="https://msdn.microsoft.com/08299592-867c-491d-9769-d16602133659">WSAStartup</a> before calling any Windows Socket functions.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSA_NOT_ENOUGH_MEMORY</a></b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory to perform the operation.

</td>
</tr>
</table>
 




## -remarks



The 
<b>WSAStringToAddress</b> function converts a network address in standard text   form into its numeric binary form in a <a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">sockaddr</a> structure.

Any missing components of the address will be defaulted to a reasonable value, if possible. For example, a missing port number will default to zero. If the caller wants the translation to be done by a particular provider, it should supply the corresponding 
<a href="https://msdn.microsoft.com/758c5553-056f-4ea5-a851-30ef641ffb14">WSAPROTOCOL_INFO</a> structure in the <i>lpProtocolInfo</i> parameter.

The 
<b>WSAStringToAddress</b> function fails (and returns WSAEINVAL) if the <b>sin_family</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff570823">SOCKADDR_IN</a> structure, which is passed in the <i>lpAddress</i> parameter in the form of a 
<b>sockaddr</b> structure, is not set to AF_INET or AF_INET6. 

Support for IPv6 addresses using the <b>WSAStringToAddress</b> function was added on Windows XP with Service Pack 1 (SP1)
  and later. IPv6 must also be installed on the local computer for the <b>WSAStringToAddress</b> function to support IPv6 addresses. 

<b>Windows Phone 8:</b> This  function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This   function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.




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



<a href="https://msdn.microsoft.com/d72e55e6-79a9-4386-9e1a-24a322f13426">WSAAddressToString</a>



<a href="https://msdn.microsoft.com/758c5553-056f-4ea5-a851-30ef641ffb14">WSAPROTOCOL_INFO</a>



<a href="https://msdn.microsoft.com/08299592-867c-491d-9769-d16602133659">WSAStartup</a>



<a href="https://msdn.microsoft.com/7d6df658-9d83-45c7-97e7-b2a016a73847">inet_addr</a>



<a href="https://msdn.microsoft.com/01cd32e7-a01d-40e8-afb5-69223d643a0e">inet_ntoa</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">sockaddr</a>
 

 

