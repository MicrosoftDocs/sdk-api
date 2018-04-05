---
UID: NS:ws2def._SOCKET_ADDRESS_LIST
title: "_SOCKET_ADDRESS_LIST"
author: windows-driver-content
description: SOCKET_ADDRESS_LIST structure stores an array of SOCKET_ADDRESS structures.
old-location: winsock\socket_address_list.htm
old-project: WinSock
ms.assetid: da727dba-3814-4b6a-bc05-ab8fbd8fbe90
ms.author: windowsdriverdev
ms.date: 3/30/2018
ms.keywords: "*LPSOCKET_ADDRESS_LIST, *PSOCKET_ADDRESS_LIST, FAR *LPSOCKET_ADDRESS_LIST, FAR *LPSOCKET_ADDRESS_LIST structure [Winsock], PSOCKET_ADDRESS_LIST, PSOCKET_ADDRESS_LIST structure pointer [Winsock], SOCKET_ADDRESS_LIST, SOCKET_ADDRESS_LIST structure [Winsock], _SOCKET_ADDRESS_LIST, winsock.socket_address_list, winsock2/FAR *LPSOCKET_ADDRESS_LIST, winsock2/PSOCKET_ADDRESS_LIST, winsock2/SOCKET_ADDRESS_LIST, ws2def/FAR *LPSOCKET_ADDRESS_LIST, ws2def/PSOCKET_ADDRESS_LIST, ws2def/SOCKET_ADDRESS_LIST"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: SOCKET_ADDRESS_LIST, *PSOCKET_ADDRESS_LIST, *LPSOCKET_ADDRESS_LIST
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ws2def.h
-	Winsock2.h
api_name:
-	SOCKET_ADDRESS_LIST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _SOCKET_ADDRESS_LIST structure


## -description


The 
<b>SOCKET_ADDRESS_LIST</b> structure stores an array of <a href="https://msdn.microsoft.com/37fbcb96-a859-4eca-8928-8051f95407b9">SOCKET_ADDRESS</a> structures that contain protocol-specific address information.
			


## -struct-fields




### -field iAddressCount

The number of address structures in the <b>Address</b> member.


### -field Address

An array of <a href="https://msdn.microsoft.com/37fbcb96-a859-4eca-8928-8051f95407b9">SOCKET_ADDRESS</a> structures that are specific to a protocol family.


## -remarks



On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>SOCKET_ADDRESS_LIST</b> structure is defined in the <i>Ws2def.h</i> header file. Note that the <i>Ws2def.h</i> header file is automatically included in <i>Winsock2.h</i>, and should never be used directly.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff570815">SIO_ADDRESS_LIST_QUERY</a>



<a href="https://msdn.microsoft.com/37fbcb96-a859-4eca-8928-8051f95407b9">SOCKET_ADDRESS</a>



<a href="https://msdn.microsoft.com/bf380ddf-8171-4ef4-be47-94c7a6aabf0a">Using SIO_ADDRESS_LIST_SORT</a>



<a href="https://msdn.microsoft.com/7323d814-e96e-44b9-8ade-a9317e4fbf17">WSAConnectByList</a>



<a href="https://msdn.microsoft.com/038aeca6-d7b7-4f74-ac69-4536c2e5118b">WSAIoctl</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566296">WSPIoctl</a>
 

 

