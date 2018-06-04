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
 

 

