---
UID: NF:winsock2.inet_ntoa
title: inet_ntoa function
author: windows-sdk-content
description: The inet_ntoa function converts an (Ipv4) Internet network address into an ASCII string in Internet standard dotted-decimal format.
old-location: winsock\inet_ntoa_2.htm
old-project: winsock
ms.assetid: 01cd32e7-a01d-40e8-afb5-69223d643a0e
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: "_win32_inet_ntoa_2, inet_ntoa, inet_ntoa function [Winsock], winsock.inet_ntoa_2, wsipv6ok/inet_ntoa"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winsock2.h
req.include-header: Winsock2.h, Winsock.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - inet_ntoa
product: Windows
targetos: Windows
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# inet_ntoa function


## -description



			The 
<b>inet_ntoa</b> function converts an (Ipv4) Internet network address into an ASCII string in Internet standard dotted-decimal format.


## -parameters




### -param in [in]

An 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556972">in_addr</a> structure that represents an Internet host address.


## -returns



If no error occurs, 
<b>inet_ntoa</b> returns a character pointer to a static buffer containing the text address in standard ".'' notation. Otherwise, it returns <b>NULL</b>.




## -remarks



The 
<b>inet_ntoa</b> function takes an Internet address structure specified by the <i>in</i> parameter and returns a <b>NULL</b>-terminated ASCII string that represents the address in "." (dot) notation as in "192.168.16.0", an example of an IPv4 address in dotted-decimal notation.   The string returned by 
<b>inet_ntoa</b> resides in memory that is allocated by Windows Sockets. The application should not make any assumptions about the way in which the memory is allocated. The string returned is guaranteed to be valid only until the next Windows Sockets function call is made within the same thread. Therefore, the data should be copied before another Windows Sockets call is made.


			The 
<a href="https://msdn.microsoft.com/d72e55e6-79a9-4386-9e1a-24a322f13426">WSAAddressToString</a> function can be used to convert a <a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">sockaddr</a> structure containing an IPv4 address to a string representation of an IPv4 address in Internet standard dotted-decimal notation. The advantage of the <b>WSAAddressToString</b>  function is that it supports both IPv4 and IPv6 addresses. Another advantage of the  <b>WSAAddressToString</b>  function is that there are both ASCII and Unicode versions of this function.

On Windows Vista and later, the <a href="https://msdn.microsoft.com/f198b770-9429-4b51-9fb4-06cf9917bc21">RtlIpv4AddressToString</a> function can be used to convert an IPv4 address represented as an <a href="https://msdn.microsoft.com/library/windows/hardware/ff556972">IN_ADDR</a> structure to a string representation of an IPv4 address in Internet standard dotted-decimal notation. On Windows Vista and later, the <a href="https://msdn.microsoft.com/a891adb0-6c2d-4b69-a0de-4a615be938e3">RtlIpv6AddressToString</a> function can be used to convert an IPv6 address represented as an <b>IN6_ADDR</b> structure to a string representation of an IPv6 address. 

<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.




## -see-also




<b>IN6_ADDR</b>



<a href="https://msdn.microsoft.com/1e26b88c-808f-4807-8641-e5c6b10853ad">InetNtop</a>



<a href="https://msdn.microsoft.com/f198b770-9429-4b51-9fb4-06cf9917bc21">RtlIpv4AddressToString</a>



<a href="https://msdn.microsoft.com/4244eaaf-8522-4edb-abb8-dc2b063c9076">RtlIpv4AddressToStringEx</a>



<a href="https://msdn.microsoft.com/79896c13-a671-423e-975e-98a4ccfa1eb8">RtlIpv4StringToAddress</a>



<a href="https://msdn.microsoft.com/72d20cf0-38ff-4c00-93ec-949aaf6f96e2">RtlIpv4StringToAddressEx</a>



<a href="https://msdn.microsoft.com/a891adb0-6c2d-4b69-a0de-4a615be938e3">RtlIpv6AddressToString</a>



<a href="https://msdn.microsoft.com/a7de2da3-21ea-42fa-9474-f33252838632">RtlIpv6AddressToStringEx</a>



<a href="https://msdn.microsoft.com/3cd3bfcf-e9b2-4ee6-8e93-a31a70fc3ad3">RtlIpv6StringToAddress</a>



<a href="https://msdn.microsoft.com/3a95c405-3f2c-4bd5-805e-3e879c4c20e2">RtlIpv6StringToAddressEx</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">SOCKADDR</a>



<a href="https://msdn.microsoft.com/d72e55e6-79a9-4386-9e1a-24a322f13426">WSAAddressToString</a>



<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/baae2bf9-f505-4365-b60e-e3247a0218c8">Winsock Reference</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556972">in_addr</a>



<a href="https://msdn.microsoft.com/7d6df658-9d83-45c7-97e7-b2a016a73847">inet_addr</a>
 

 

