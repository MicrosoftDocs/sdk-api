---
UID: NS:ws2def._SOCKET_ADDRESS
title: "_SOCKET_ADDRESS"
author: windows-sdk-content
description: SOCKET_ADDRESS structure stores protocol-specific address information.
old-location: winsock\socket_address_2.htm
old-project: WinSock
ms.assetid: 37fbcb96-a859-4eca-8928-8051f95407b9
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: "*LPSOCKET_ADDRESS, *PSOCKET_ADDRESS, PSOCKET_ADDRESS, PSOCKET_ADDRESS structure pointer [Winsock], SOCKET_ADDRESS, SOCKET_ADDRESS structure [Winsock], _SOCKET_ADDRESS, _win32_socket_address_2, winsock.socket_address_2, winsock2/PSOCKET_ADDRESS, winsock2/SOCKET_ADDRESS, ws2def/PSOCKET_ADDRESS, ws2def/SOCKET_ADDRESS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ws2def.h
req.include-header: Winsock2.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wrdsgraphicschannels.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SOCKET_ADDRESS, *PSOCKET_ADDRESS, *LPSOCKET_ADDRESS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ws2def.h
 - Winsock2.h
api_name:
 - SOCKET_ADDRESS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
 

 

