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

# _HTTP_TRANSPORT_ADDRESS structure


## -description


The 
<b>HTTP_TRANSPORT_ADDRESS</b> structure specifies the addresses (local and remote) used for a particular HTTP connection.


## -struct-fields




### -field pRemoteAddress

A pointer to the remote IP address associated with this connection. For more information about how to access this address, see the Remarks section.


### -field pLocalAddress

A pointer to the local IP address associated with this connection. For more information about how to access this address, see the Remarks section.


## -remarks



Although the <b>pRemoteAddress</b> and <b>pLocalAddress</b> members are formally declared as <b>PSOCKADDR</b>, they are in fact <b>PSOCKADDR_IN</b> or <b>PSOCKADDR_IN6</b> types. Inspect the <b>sa_family</b> member, which is the same in all three structures, to determine how to access the address. If <b>sa_family</b> is equal to AF_INET, then the address is in IPv4 form and can be accessed by casting the members to <b>PSOCKADDR_IN</b>, but if <b>sa_family</b> equals AF_INET6, the address is in IPv6 form and you must cast them to <b>PSOCKADDR_IN6</b> before accessing the address. Both <b>pLocalAddress</b> and <b>pRemoteAddress</b> are always of the same type; that is they are either both of type <b>PSOCKADDR_IN</b> or both of type <b>PSOCKADDR_IN6</b>.




## -see-also




<a href="https://msdn.microsoft.com/e38f7a05-f966-4853-be3b-5cdbf224719e">HTTP Server API Version 1.0 Structures</a>



<a href="https://msdn.microsoft.com/e592cf54-df6d-472b-a736-c44a5ccdd3d2">HTTP_REQUEST</a>
 

 

