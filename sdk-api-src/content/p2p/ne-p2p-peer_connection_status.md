---
UID: NE:p2p.peer_connection_status_tag
title: PEER_CONNECTION_STATUS (p2p.h)
description: The PEER_CONNECTION_STATUS enumeration specifies the status of a peer direct or neighbor connection.
helpviewer_keywords: ["PEER_CONNECTED","PEER_CONNECTION_FAILED","PEER_CONNECTION_STATUS","PEER_CONNECTION_STATUS enumeration [Peer Networking]","PEER_DISCONNECTED","p2p.peer_connection_status","p2p/PEER_CONNECTED","p2p/PEER_CONNECTION_FAILED","p2p/PEER_CONNECTION_STATUS","p2p/PEER_DISCONNECTED"]
old-location: p2p\peer_connection_status.htm
tech.root: p2p
ms.assetid: 42095744-bcbf-433f-b631-2281f079d2fd
ms.date: 12/05/2018
ms.keywords: PEER_CONNECTED, PEER_CONNECTION_FAILED, PEER_CONNECTION_STATUS, PEER_CONNECTION_STATUS enumeration [Peer Networking], PEER_DISCONNECTED, p2p.peer_connection_status, p2p/PEER_CONNECTED, p2p/PEER_CONNECTION_FAILED, p2p/PEER_CONNECTION_STATUS, p2p/PEER_DISCONNECTED
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
req.typenames: PEER_CONNECTION_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_connection_status_tag
 - p2p/peer_connection_status_tag
 - PEER_CONNECTION_STATUS
 - p2p/PEER_CONNECTION_STATUS
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
 - PEER_CONNECTION_STATUS
---

# PEER_CONNECTION_STATUS enumeration


## -description

The <b>PEER_CONNECTION_STATUS</b> enumeration specifies the status of a peer direct or neighbor connection.

## -enum-fields

### -field PEER_CONNECTED:1

The peer is connected to another peer.

### -field PEER_DISCONNECTED:2

The peer has disconnected from another peer.

### -field PEER_CONNECTION_FAILED:3

The peer failed to connect to another peer.

