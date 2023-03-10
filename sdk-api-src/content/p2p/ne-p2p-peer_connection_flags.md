---
UID: NE:p2p.peer_connection_flags_tag
title: PEER_CONNECTION_FLAGS (p2p.h)
description: The PEER_CONNECTION_FLAGS enumeration specifies the types of connections that a peer can have.
helpviewer_keywords: ["PEER_CONNECTION_DIRECT","PEER_CONNECTION_FLAGS","PEER_CONNECTION_FLAGS enumeration [Peer Networking]","PEER_CONNECTION_NEIGHBOR","p2p.peer_connection_flags","p2p/PEER_CONNECTION_DIRECT","p2p/PEER_CONNECTION_FLAGS","p2p/PEER_CONNECTION_NEIGHBOR"]
old-location: p2p\peer_connection_flags.htm
tech.root: p2p
ms.assetid: 24723421-18e4-4333-8c25-f5ee08182f7f
ms.date: 12/05/2018
ms.keywords: PEER_CONNECTION_DIRECT, PEER_CONNECTION_FLAGS, PEER_CONNECTION_FLAGS enumeration [Peer Networking], PEER_CONNECTION_NEIGHBOR, p2p.peer_connection_flags, p2p/PEER_CONNECTION_DIRECT, p2p/PEER_CONNECTION_FLAGS, p2p/PEER_CONNECTION_NEIGHBOR
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
req.typenames: PEER_CONNECTION_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_connection_flags_tag
 - p2p/peer_connection_flags_tag
 - PEER_CONNECTION_FLAGS
 - p2p/PEER_CONNECTION_FLAGS
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
 - PEER_CONNECTION_FLAGS
---

# PEER_CONNECTION_FLAGS enumeration


## -description

The <b>PEER_CONNECTION_FLAGS</b> enumeration specifies the types of connections that a peer can have.

## -enum-fields

### -field PEER_CONNECTION_NEIGHBOR:0x0001

Specifies that a connection is a neighbor connection.

### -field PEER_CONNECTION_DIRECT:0x0002

Specifies that a connection is a direct connection to another node.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_connection_info">PEER_CONNECTION_INFO</a>
