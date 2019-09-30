---
UID: NS:p2p.peer_address_tag
title: PEER_ADDRESS (p2p.h)
author: windows-sdk-content
description: The PEER_ADDRESS structure specifies the information about the IP address.
old-location: p2p\peer_address.htm
tech.root: P2PSdk
ms.assetid: 09476d3b-ec65-40a2-90ee-a20be230deca
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PPEER_ADDRESS, PEER_ADDRESS, PEER_ADDRESS structure [Peer Networking], PPEER_ADDRESS, PPEER_ADDRESS structure pointer [Peer Networking], p2p.peer_address, p2p/PPEER_ADDRESS, p2p/peer_address_tag"
ms.topic: struct
f1_keywords: 
 - "p2p/PEER_ADDRESS"
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
 - PEER_ADDRESS
targetos: Windows
req.typenames: PEER_ADDRESS, *PPEER_ADDRESS
req.redist: 
ms.custom: 19H1
---

# PEER_ADDRESS structure


## -description


The <b>PEER_ADDRESS</b> structure specifies the  information about the IP address.


## -struct-fields




### -field dwSize

Specifies the size of this structure.


### -field sin6

Specifies the IP address of the node in the Peer Infrastructure.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/p2p/ns-p2p-peer_connection_info_tag">PEER_CONNECTION_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/p2p/ns-p2p-peer_member">PEER_MEMBER</a>



<a href="https://docs.microsoft.com/windows/desktop/api/p2p/ns-p2p-peer_node_info">PEER_NODE_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/p2p/nf-p2p-peergraphconnect">PeerGraphConnect</a>



<a href="https://docs.microsoft.com/windows/desktop/api/p2p/nf-p2p-peergraphopendirectconnection">PeerGraphOpenDirectConnection</a>



<a href="https://docs.microsoft.com/windows/desktop/api/p2p/nf-p2p-peergroupopendirectconnection">PeerGroupOpenDirectConnection</a>
 

 

