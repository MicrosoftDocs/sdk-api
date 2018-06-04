---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _SOCKET_ADDRESS structure


## -description



			The 
<b>SOCKET_ADDRESS</b> structure stores protocol-specific address information.


## -struct-fields




### -field lpSockaddr

A pointer to a socket address  represented as a <a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">SOCKADDR</a> structure.


### -field iSockaddrLength

The length, in bytes, of the socket address.


## -remarks



The <a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">SOCKADDR</a> structure pointed to by the <b>lpSockaddr</b> member varies depending on the protocol or address family selected. For example, the <b>sockaddr_in6</b> structure is used for an IPv6 socket address while the <b>sockaddr_in4</b> structure is used for an IPv4 socket address. The address family is the first member of all of the <b>SOCKADDR</b> structures. The address family is used to determine which structure is used. 

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>SOCKET_ADDRESS</b> structure is defined in the <i>Ws2def.h</i> header file. Note that the <i>Ws2def.h</i> header file is automatically included in <i>Winsock2.h</i>, and should never be used directly.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">SOCKADDR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570826">SOCKET_ADDRESS_LIST</a>



<a href="https://msdn.microsoft.com/bf380ddf-8171-4ef4-be47-94c7a6aabf0a">Using SIO_ADDRESS_LIST_SORT</a>



<a href="https://msdn.microsoft.com/038aeca6-d7b7-4f74-ac69-4536c2e5118b">WSAIoctl</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566296">WSPIoctl</a>
 

 

