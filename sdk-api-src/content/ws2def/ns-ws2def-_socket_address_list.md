---
UID: NS:ws2def._SOCKET_ADDRESS_LIST
title: "_SOCKET_ADDRESS_LIST"
author: windows-driver-content
description: The SOCKET_ADDRESS_LIST structure defines a variable-sized list of transport addresses.
old-location: netvista\socket_address_list.htm
old-project: netvista
ms.assetid: b005200b-b0c2-4f19-8765-cd26fbfc0cff
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: "*LPSOCKET_ADDRESS_LIST, *PSOCKET_ADDRESS_LIST, LPSOCKET_ADDRESS_LIST, LPSOCKET_ADDRESS_LIST structure pointer [Network Drivers Starting with Windows Vista], PSOCKET_ADDRESS_LIST, PSOCKET_ADDRESS_LIST structure pointer [Network Drivers Starting with Windows Vista], SOCKET_ADDRESS_LIST, SOCKET_ADDRESS_LIST structure [Network Drivers Starting with Windows Vista], _SOCKET_ADDRESS_LIST, netvista.socket_address_list, ws2def/LPSOCKET_ADDRESS_LIST, ws2def/PSOCKET_ADDRESS_LIST, ws2def/SOCKET_ADDRESS_LIST, wskref_7bca89ec-9ce8-4046-9bf6-fcaa01a37b21.xml"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ws2def.h
req.include-header: Wsk.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows Vista and later versions of the Windows operating   systems.
req.target-min-winversvr: 
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
-	ws2def.h
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


The SOCKET_ADDRESS_LIST structure defines a variable-sized list of transport addresses.


## -struct-fields




### -field iAddressCount

The number of transport addresses in the list.


### -field Address

A variable-sized array of SOCKET_ADDRESS structures. The SOCKET_ADDRESS structure is defined as
     follows:
     

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>typedef struct _SOCKET_ADDRESS {
  LPSOCKADDR  lpSockaddr;
  INT  iSockaddrLength;
} SOCKET_ADDRESS, *PSOCKET_ADDRESS, *LPSOCKET_ADDRESS;</pre>
</td>
</tr>
</table></span></div>




#### lpSockaddr

A pointer to a buffer that contains a transport address.



#### iSockaddrLength

The size, in bytes, of the SOCKADDR structure type that is pointed to by the 
       <b>lpSockaddr</b> member.


## -remarks



A WSK application passes a buffer to the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff571127">WskControlSocket</a> function when the WSK
    application queries the current list of local transport addresses that match a socket's address family.
    If the call to the 
    <b>WskControlSocket</b> function succeeds, the buffer contains a SOCKET_ADDRESS_LIST structure followed by
    the SOCKADDR structures for each of the local transport addresses that match the socket's address family.
    The WSK subsystem fills in the 
    <b>Address</b> array and sets the 
    <b>iAddressCount</b> member to the number of entries in the array. The 
    <b>lpSockaddr</b> pointers in each of the SOCKET_ADDRESS structures in the array point to the specific
    SOCKADDR structure type that corresponds to the address family that the WSK application specified when it
    created the socket.

For more information about querying the current list of local transport addresses, see 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff570815">SIO_ADDRESS_LIST_QUERY</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff570815">SIO_ADDRESS_LIST_QUERY</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">SOCKADDR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff571127">WskControlSocket</a>
 

 

