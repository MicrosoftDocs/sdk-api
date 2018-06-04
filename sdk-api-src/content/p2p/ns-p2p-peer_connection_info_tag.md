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

# peer_connection_info_tag structure


## -description


The <b>PEER_CONNECTION_INFO</b> structure contains information about a connection. This structure is returned when you are enumerating peer graphing or grouping connections.


## -struct-fields




### -field dwSize

Specifies the size a structure.


### -field dwFlags

Specifies the type of connection to a remote node. Valid values are specified by <a href="https://msdn.microsoft.com/24723421-18e4-4333-8c25-f5ee08182f7f">PEER_CONNECTION_FLAGS</a>. 


### -field ullConnectionId

Specifies the  unique ID of a connection.


### -field ullNodeId

Specifies the  unique ID of a node.


### -field pwzPeerId

Points to a string that identifies the node on the other end of a connection.


### -field address

Specifies the address of a remote node. The address is contained in a <a href="https://msdn.microsoft.com/09476d3b-ec65-40a2-90ee-a20be230deca">PEER_ADDRESS</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/09476d3b-ec65-40a2-90ee-a20be230deca">PEER_ADDRESS</a>



<a href="https://msdn.microsoft.com/ef4ea3e2-fd71-48d8-a9a8-db38ef06df20">PeerGraphEnumConnections</a>



<a href="https://msdn.microsoft.com/84a26066-3d6a-44c8-86a1-b3f997c17739">PeerGroupEnumConnections</a>
 

 

