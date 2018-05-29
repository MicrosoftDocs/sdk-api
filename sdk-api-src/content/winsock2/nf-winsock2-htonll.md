---
UID: NF:winsock2.htonll
title: htonll function
author: windows-sdk-content
description: Converts an unsigned __int64 from host to TCP/IP network byte order (which is big-endian).
old-location: winsock\htonll.htm
old-project: WinSock
ms.assetid: 3155C55D-681E-4D6D-9DFF-219465F04E4A
ms.author: windowssdkdev
ms.date: 04/30/2018
ms.keywords: htonll, htonll function [Winsock], winsock.htonll, winsock2/htonll
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winsock2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1, Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
-	HeaderDef
api_location:
-	Winsock2.h
api_name:
-	htonll
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# htonll function


## -description


The 
<b>htonll</b> inline function converts an <b>unsigned __int64</b> from host to TCP/IP network byte order (which is big-endian).


## -parameters




### -param Value

TBD




#### - value

A 64-bit unsigned number in host byte order.


## -returns




						The 
<b>htonll</b> function returns the value in TCP/IP's network byte order.




## -remarks



The 
<b>htonll</b> inline function takes a 64-bit number in host byte order and returns a 64-bit number in the network byte order used in TCP/IP networks (the AF_INET or AF_INET6 address family).

The 
<b>htonll</b> inline function can be used to convert an IPv4 address in host byte order to the IPv4 address in network byte order. This function does not do any checking to determine if the <i>value</i> parameter is a valid IPv4 address.

The <b>htonll</b>
			inline function does not require that the Winsock DLL has previously been loaded with a successful 
call to the <a href="https://msdn.microsoft.com/08299592-867c-491d-9769-d16602133659">WSAStartup</a> function.

<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

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



<a href="https://msdn.microsoft.com/3dae2655-2b3c-41d9-9650-125ac393d64a">htons</a>



<a href="https://msdn.microsoft.com/7d6df658-9d83-45c7-97e7-b2a016a73847">inet_addr</a>



<a href="https://msdn.microsoft.com/01cd32e7-a01d-40e8-afb5-69223d643a0e">inet_ntoa</a>



<a href="https://msdn.microsoft.com/00176446-517B-40B8-AF9A-D61B5B033AE1">ntohd</a>



<a href="https://msdn.microsoft.com/FD98AE9D-C753-479C-BF44-7495B3B5C953">ntohf</a>



<a href="https://msdn.microsoft.com/04673bef-22c6-424f-a5ae-689fb648b54e">ntohl</a>



<a href="https://msdn.microsoft.com/90C582C4-01C4-4D8B-8AD6-F65F96DABA7E">ntohll</a>



<a href="https://msdn.microsoft.com/9946df13-3b40-4bcb-91ca-10684b3fc9a5">ntohs</a>
 

 

