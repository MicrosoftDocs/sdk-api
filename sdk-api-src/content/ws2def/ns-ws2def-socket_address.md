---
UID: NS:ws2def._SOCKET_ADDRESS
title: SOCKET_ADDRESS (ws2def.h)
description: SOCKET_ADDRESS structure stores protocol-specific address information.
helpviewer_keywords: ["*LPSOCKET_ADDRESS","*PSOCKET_ADDRESS","PSOCKET_ADDRESS","PSOCKET_ADDRESS structure pointer [Winsock]","SOCKET_ADDRESS","SOCKET_ADDRESS structure [Winsock]","_win32_socket_address_2","winsock.socket_address_2","winsock2/PSOCKET_ADDRESS","winsock2/SOCKET_ADDRESS","ws2def/PSOCKET_ADDRESS","ws2def/SOCKET_ADDRESS"]
old-location: winsock\socket_address_2.htm
tech.root: WinSock
ms.assetid: 37fbcb96-a859-4eca-8928-8051f95407b9
ms.date: 12/05/2018
ms.keywords: '*LPSOCKET_ADDRESS, *PSOCKET_ADDRESS, PSOCKET_ADDRESS, PSOCKET_ADDRESS structure pointer [Winsock], SOCKET_ADDRESS, SOCKET_ADDRESS structure [Winsock], _win32_socket_address_2, winsock.socket_address_2, winsock2/PSOCKET_ADDRESS, winsock2/SOCKET_ADDRESS, ws2def/PSOCKET_ADDRESS, ws2def/SOCKET_ADDRESS'
req.header: ws2def.h
req.include-header: Winsock2.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
targetos: Windows
req.typenames: SOCKET_ADDRESS, *PSOCKET_ADDRESS, *LPSOCKET_ADDRESS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SOCKET_ADDRESS
 - ws2def/_SOCKET_ADDRESS
 - PSOCKET_ADDRESS
 - ws2def/PSOCKET_ADDRESS
 - SOCKET_ADDRESS
 - ws2def/SOCKET_ADDRESS
dev_langs:
 - c++
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
---

# SOCKET_ADDRESS structure


## -description

The 
<b>SOCKET_ADDRESS</b> structure stores protocol-specific address information.

## -struct-fields

### -field lpSockaddr

A pointer to a socket address  represented as a <a href="/windows/desktop/WinSock/sockaddr-2">SOCKADDR</a> structure.

### -field iSockaddrLength

The length, in bytes, of the socket address.

## -remarks

The <a href="/windows/desktop/WinSock/sockaddr-2">SOCKADDR</a> structure pointed to by the <b>lpSockaddr</b> member varies depending on the protocol or address family selected. For example, the <b>sockaddr_in6</b> structure is used for an IPv6 socket address while the <b>sockaddr_in4</b> structure is used for an IPv4 socket address. The address family is the first member of all of the <b>SOCKADDR</b> structures. The address family is used to determine which structure is used. 

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>SOCKET_ADDRESS</b> structure is defined in the <i>Ws2def.h</i> header file. Note that the <i>Ws2def.h</i> header file is automatically included in <i>Winsock2.h</i>, and should never be used directly.

## -see-also

<a href="/windows/desktop/WinSock/sockaddr-2">SOCKADDR</a>



<a href="/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)">SOCKET_ADDRESS_LIST</a>



<a href="/windows/desktop/WinSock/using-sio-address-list-sort">Using SIO_ADDRESS_LIST_SORT</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a>



<a href="/previous-versions/windows/hardware/network/ff566296(v=vs.85)">LPWSPIoctl</a>