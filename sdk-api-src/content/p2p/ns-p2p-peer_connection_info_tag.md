---
UID: NS:p2p.peer_connection_info_tag
title: peer_connection_info_tag
author: windows-sdk-content
description: The PEER_CONNECTION_INFO structure contains information about a connection. This structure is returned when you are enumerating peer graphing or grouping connections.
old-location: p2p\peer_connection_info.htm
tech.root: p2psdk
ms.assetid: 039fa00e-c193-46fd-b7e6-41eb7baeab3e
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: PEER_CONNECTION_INFO, PEER_CONNECTION_INFO structure [Peer Networking], p2p.peer_connection_info, p2p/peer_connection_info_tag, peer_connection_info_tag
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only],Windows XP with SP1 with the Advanced Networking Pack forWindows XP
req.target-min-winversvr: None supported
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
 - P2P.h
api_name:
 - PEER_CONNECTION_INFO
product: Windows
targetos: Windows
req.typenames: PEER_CONNECTION_INFO
req.redist: 
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
 

 

