---
UID: NS:p2p.peer_node_info_tag
title: PEER_NODE_INFO (p2p.h)
description: The PEER_NODE_INFO structure contains information that is specific to a particular node in a peer graph.
helpviewer_keywords: ["*PPEER_NODE_INFO","PEER_NODE_INFO","PEER_NODE_INFO structure [Peer Networking]","PPEER_NODE_INFO","PPEER_NODE_INFO structure pointer [Peer Networking]","p2p.peer_node_info","p2p/PPEER_NODE_INFO","p2p/peer_node_info_tag"]
old-location: p2p\peer_node_info.htm
tech.root: p2p
ms.assetid: 51cc6c27-91ca-4d02-95d6-207827450fd5
ms.date: 12/05/2018
ms.keywords: '*PPEER_NODE_INFO, PEER_NODE_INFO, PEER_NODE_INFO structure [Peer Networking], PPEER_NODE_INFO, PPEER_NODE_INFO structure pointer [Peer Networking], p2p.peer_node_info, p2p/PPEER_NODE_INFO, p2p/peer_node_info_tag'
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
req.typenames: PEER_NODE_INFO, *PPEER_NODE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_node_info_tag
 - p2p/peer_node_info_tag
 - PPEER_NODE_INFO
 - p2p/PPEER_NODE_INFO
 - PEER_NODE_INFO
 - p2p/PEER_NODE_INFO
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
 - PEER_NODE_INFO
---

# PEER_NODE_INFO structure


## -description

The <b>PEER_NODE_INFO</b> structure contains information that is specific to a particular node in a peer graph.

## -struct-fields

### -field dwSize

Specifies the size of the data structure. Set the value to   sizeof(<b>PEER_NODE_INFO</b>). This member is required and has no default value.

### -field ullNodeId

Specifies a unique ID that identifies an application's  connection to its neighbor. An application cannot set the value of this member, it is created by the Peer Graphing Infrastructure.

### -field pwzPeerId

Specifies the ID of this peer. This value is set for the application by the Peer Graphing Infrastructure. when the application creates or opens a peer graph.

### -field cAddresses

Specifies the number of addresses in <b>pAddresses</b>. This member is required and has no default value.

### -field pAddresses

Points to  an array of <a href="/windows/desktop/api/p2p/ns-p2p-peer_address">PEER_ADDRESS</a> structures that indicate which addresses and  ports this instance is listening to for group traffic. This member is required and has no default value.

### -field pwzAttributes

Points to a string  that contains the  attributes that describe this particular node. This string is a free-form text string that is specific to the application. This parameter is optional; the default value is <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_address">PEER_ADDRESS</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphgetnodeinfo">PeerGraphGetNodeInfo</a>