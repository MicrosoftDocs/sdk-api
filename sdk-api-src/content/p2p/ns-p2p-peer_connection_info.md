---
UID: NS:p2p.peer_connection_info_tag
title: PEER_CONNECTION_INFO (p2p.h)
description: The PEER_CONNECTION_INFO structure contains information about a connection. This structure is returned when you are enumerating peer graphing or grouping connections.
helpviewer_keywords: ["PEER_CONNECTION_INFO","PEER_CONNECTION_INFO structure [Peer Networking]","p2p.peer_connection_info","p2p/peer_connection_info_tag"]
old-location: p2p\peer_connection_info.htm
tech.root: p2p
ms.assetid: 039fa00e-c193-46fd-b7e6-41eb7baeab3e
ms.date: 12/05/2018
ms.keywords: PEER_CONNECTION_INFO, PEER_CONNECTION_INFO structure [Peer Networking], p2p.peer_connection_info, p2p/peer_connection_info_tag
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
targetos: Windows
req.typenames: PEER_CONNECTION_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_connection_info_tag
 - p2p/peer_connection_info_tag
 - PEER_CONNECTION_INFO
 - p2p/PEER_CONNECTION_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - P2P.h
api_name:
 - PEER_CONNECTION_INFO
---

# PEER_CONNECTION_INFO structure


## -description

The <b>PEER_CONNECTION_INFO</b> structure contains information about a connection. This structure is returned when you are enumerating peer graphing or grouping connections.

## -struct-fields

### -field dwSize

Specifies the size a structure.

### -field dwFlags

Specifies the type of connection to a remote node. Valid values are specified by <a href="/windows/desktop/api/p2p/ne-p2p-peer_connection_flags">PEER_CONNECTION_FLAGS</a>.

### -field ullConnectionId

Specifies the  unique ID of a connection.

### -field ullNodeId

Specifies the  unique ID of a node.

### -field pwzPeerId

Points to a string that identifies the node on the other end of a connection.

### -field address

Specifies the address of a remote node. The address is contained in a <a href="/windows/desktop/api/p2p/ns-p2p-peer_address">PEER_ADDRESS</a> structure.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_address">PEER_ADDRESS</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphenumconnections">PeerGraphEnumConnections</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupenumconnections">PeerGroupEnumConnections</a>