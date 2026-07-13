---
UID: NE:p2p.peer_group_status_tag
title: PEER_GROUP_STATUS (p2p.h)
description: The PEER_GROUP_STATUS flags indicate whether or not the peer group has connections present.
helpviewer_keywords: ["PEER_GROUP_STATUS","PEER_GROUP_STATUS enumeration [Peer Networking]","PEER_GROUP_STATUS_HAS_CONNECTIONS","PEER_GROUP_STATUS_LISTENING","p2p.peer_group_status","p2p/PEER_GROUP_STATUS","p2p/PEER_GROUP_STATUS_HAS_CONNECTIONS","p2p/PEER_GROUP_STATUS_LISTENING"]
old-location: p2p\peer_group_status.htm
tech.root: p2p
ms.assetid: ed3fa9a6-5180-419f-b5d1-02889bbcdd0d
ms.date: 12/05/2018
ms.keywords: PEER_GROUP_STATUS, PEER_GROUP_STATUS enumeration [Peer Networking], PEER_GROUP_STATUS_HAS_CONNECTIONS, PEER_GROUP_STATUS_LISTENING, p2p.peer_group_status, p2p/PEER_GROUP_STATUS, p2p/PEER_GROUP_STATUS_HAS_CONNECTIONS, p2p/PEER_GROUP_STATUS_LISTENING
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only],Windows XP with SP1with the Advanced Networking Pack forWindows XP
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
req.typenames: PEER_GROUP_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_group_status_tag
 - p2p/peer_group_status_tag
 - PEER_GROUP_STATUS
 - p2p/PEER_GROUP_STATUS
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
 - PEER_GROUP_STATUS
---

# PEER_GROUP_STATUS enumeration


## -description

The <b>PEER_GROUP_STATUS</b> flags indicate whether or not the peer group has connections present.

## -enum-fields

### -field PEER_GROUP_STATUS_LISTENING:0x0001

The peer group is awaiting new connections.

### -field PEER_GROUP_STATUS_HAS_CONNECTIONS:0x0002

The peer group has at least one connection.

## -see-also

[PEER_GROUP_EVENT_DATA](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1)



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupgetstatus">PeerGroupGetStatus</a>
