---
UID: NF:winsock2.ntohf
title: ntohf function
author: windows-sdk-content
description: Converts an unsigned __int32 from TCP/IP network order to host byte order (which is little-endian on Intel processors) and returns a float.
old-location: winsock\ntohf.htm
tech.root: winsock
ms.assetid: FD98AE9D-C753-479C-BF44-7495B3B5C953
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ntohf, ntohf function [Winsock], winsock.ntohf, winsock2/ntohf
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winsock2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1, Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winsock2.h
api_name:
 - ntohf
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ntohf function


## -description


The 
<b>ntohf</b> inline function converts an <b>unsigned __int32</b> from TCP/IP network order to host byte order (which is little-endian on Intel processors) and returns a <b>float</b>.


## -parameters




### -param Value

An  <b>unsigned __int32</b> number in TCP/IP network byte order.


## -returns



The 
<b>ntohf</b> function returns the value supplied in the <i>value</i> parameter with the byte order reversed. If  <i>value</i> is already in host byte order, then this function will reverse it. It is up to the application to determine if the byte order must be reversed.




## -remarks



The 
<b>ntohf</b> inline function takes an <b>unsigned __int32</b> in TCP/IP network byte order (the AF_INET or AF_INET6 address family) and returns a <b>float</b> that contains a number in host byte order. 

The 
<b>ntohf</b> function can be used to convert an IPv4 address in network byte order to the IPv4 address in host byte order. This function does not do any checking to determine if the <i>value</i> parameter is a valid IPv4 address.

The <b>ntohf</b>function does not require that the Winsock DLL has previously been loaded with a successful 
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



<a href="https://msdn.microsoft.com/3155C55D-681E-4D6D-9DFF-219465F04E4A">htonll</a>



<a href="https://msdn.microsoft.com/3dae2655-2b3c-41d9-9650-125ac393d64a">htons</a>



<a href="https://msdn.microsoft.com/7d6df658-9d83-45c7-97e7-b2a016a73847">inet_addr</a>



<a href="https://msdn.microsoft.com/01cd32e7-a01d-40e8-afb5-69223d643a0e">inet_ntoa</a>



<a href="https://msdn.microsoft.com/00176446-517B-40B8-AF9A-D61B5B033AE1">ntohd</a>



<a href="https://msdn.microsoft.com/04673bef-22c6-424f-a5ae-689fb648b54e">ntohl</a>



<a href="https://msdn.microsoft.com/90C582C4-01C4-4D8B-8AD6-F65F96DABA7E">ntohll</a>



<a href="https://msdn.microsoft.com/9946df13-3b40-4bcb-91ca-10684b3fc9a5">ntohs</a>
 

 

