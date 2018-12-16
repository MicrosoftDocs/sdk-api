---
UID: NF:winsock.ntohl
title: ntohl function
author: windows-sdk-content
description: The ntohl function converts a u_long from TCP/IP network order to host byte order (which is little-endian on Intel processors).
old-location: winsock\ntohl_2.htm
tech.root: winsock
ms.assetid: 04673bef-22c6-424f-a5ae-689fb648b54e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_win32_ntohl_2, ntohl, ntohl function [Winsock], winsock.ntohl_2, winsock/ntohl"
ms.topic: function
req.header: winsock.h
req.include-header: Winsock2.h
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
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - ntohl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ntohl function


## -description


The 
<b>ntohl</b> function converts a <b>u_long</b> from TCP/IP network order to host byte order (which is little-endian on Intel processors).


## -parameters




### -param netlong [in]

A 32-bit number in TCP/IP network byte order.


## -returns



The 
<b>ntohl</b> function returns the value supplied in the <i>netlong</i> parameter with the byte order reversed. If  <i>netlong</i> is already in host byte order, then this function will reverse it. It is up to the application to determine if the byte order must be reversed.




## -remarks



The 
<b>ntohl</b> function takes a 32-bit number in TCP/IP network byte order (the AF_INET or AF_INET6 address family) and returns a 32-bit number in host byte order. 

The 
<b>ntohl</b> function can be used to convert an IPv4 address in network byte order to the IPv4 address in host byte order. This function does not do any checking to determine if the <i>netlong</i> parameter is a valid IPv4 address.

The <b>ntohl</b>function does not require that the Winsock DLL has previously been loaded with a successful 
call to the <a href="https://msdn.microsoft.com/08299592-867c-491d-9769-d16602133659">WSAStartup</a> function.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.




## -see-also




<a href="https://msdn.microsoft.com/1e26b88c-808f-4807-8641-e5c6b10853ad">InetNtop</a>



<a href="https://msdn.microsoft.com/d0705997-0dc7-443b-a43f-611301cc9169">InetPton</a>



<a href="https://msdn.microsoft.com/33512f49-d576-4439-ad8d-5c87387d6214">WSAHtonl</a>



<a href="https://msdn.microsoft.com/95fb103b-f7dd-4fa4-bf68-ed8e87cdd96b">WSAHtons</a>



<a href="https://msdn.microsoft.com/7e3b42eb-3b93-459f-828a-c19e277882c7">WSANtohl</a>



<a href="https://msdn.microsoft.com/0a4bc3a9-9919-4dcb-8a37-af37e0243c8f">WSANtohs</a>



<a href="https://msdn.microsoft.com/DEC42B75-F637-4CD5-B42F-4F59D1516BB9">htond</a>



<a href="https://msdn.microsoft.com/93011B2E-2B3C-4EDD-90F7-82A11542A154">htonf</a>



<a href="https://msdn.microsoft.com/e3a18c5e-7efb-43d9-9abc-9d573bbb1923">htonl</a>



<a href="https://msdn.microsoft.com/3155C55D-681E-4D6D-9DFF-219465F04E4A">htonll</a>



<a href="https://msdn.microsoft.com/3dae2655-2b3c-41d9-9650-125ac393d64a">htons</a>



<a href="https://msdn.microsoft.com/7d6df658-9d83-45c7-97e7-b2a016a73847">inet_addr</a>



<a href="https://msdn.microsoft.com/01cd32e7-a01d-40e8-afb5-69223d643a0e">inet_ntoa</a>



<a href="https://msdn.microsoft.com/00176446-517B-40B8-AF9A-D61B5B033AE1">ntohd</a>



<a href="https://msdn.microsoft.com/FD98AE9D-C753-479C-BF44-7495B3B5C953">ntohf</a>



<a href="https://msdn.microsoft.com/9946df13-3b40-4bcb-91ca-10684b3fc9a5">ntohs</a>
 

 

