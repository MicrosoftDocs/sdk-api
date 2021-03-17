---
UID: NS:p2p.peer_event_synchronized_data_tag
title: PEER_EVENT_SYNCHRONIZED_DATA (p2p.h)
description: The PEER_EVENT_SYNCHRONIZED_DATA is pointed to by a PEER_GRAPH_EVENT_DATA structure's union if a PEER_GRAPH_EVENT_RECORD_CHANGE or PEER_GROUP_EVENT_RECORD_CHANGE event is triggered.
helpviewer_keywords: ["*PPEER_EVENT_SYNCHRONIZED_DATA","PEER_EVENT_SYNCHRONIZED_DATA","PEER_EVENT_SYNCHRONIZED_DATA structure [Peer Networking]","PPEER_EVENT_SYNCHRONIZED_DATA","PPEER_EVENT_SYNCHRONIZED_DATA structure pointer [Peer Networking]","p2p.peer_event_synchronized_data","p2p/PPEER_EVENT_SYNCHRONIZED_DATA","p2p/peer_event_synchronized_data_tag"]
old-location: p2p\peer_event_synchronized_data.htm
tech.root: p2p
ms.assetid: ae7dc220-a827-4671-97b3-1ac039ab3e08
ms.date: 12/05/2018
ms.keywords: '*PPEER_EVENT_SYNCHRONIZED_DATA, PEER_EVENT_SYNCHRONIZED_DATA, PEER_EVENT_SYNCHRONIZED_DATA structure [Peer Networking], PPEER_EVENT_SYNCHRONIZED_DATA, PPEER_EVENT_SYNCHRONIZED_DATA structure pointer [Peer Networking], p2p.peer_event_synchronized_data, p2p/PPEER_EVENT_SYNCHRONIZED_DATA, p2p/peer_event_synchronized_data_tag'
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
req.typenames: PEER_EVENT_SYNCHRONIZED_DATA, *PPEER_EVENT_SYNCHRONIZED_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_event_synchronized_data_tag
 - p2p/peer_event_synchronized_data_tag
 - PPEER_EVENT_SYNCHRONIZED_DATA
 - p2p/PPEER_EVENT_SYNCHRONIZED_DATA
 - PEER_EVENT_SYNCHRONIZED_DATA
 - p2p/PEER_EVENT_SYNCHRONIZED_DATA
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
 - PEER_EVENT_SYNCHRONIZED_DATA
---

# PEER_EVENT_SYNCHRONIZED_DATA structure


## -description

The <b>PEER_EVENT_SYNCHRONIZED_DATA</b> is pointed to by a <a href="/windows/desktop/api/p2p/ns-p2p-peer_graph_event_data">PEER_GRAPH_EVENT_DATA</a> structure's union if a PEER_GRAPH_EVENT_RECORD_CHANGE or  PEER_GROUP_EVENT_RECORD_CHANGE event is triggered. The <b>PEER_EVENT_SYNCHRONIZED_DATA</b> structure indicates the type of record that has been synchronized.

## -struct-fields

### -field dwSize

Specifies the size of the structure.

### -field recordType

Specifies the type of record that is being synchronized.

## -remarks

This event only occurs if an application has specified a record synchronization precedence in a previous call to <a href="/windows/desktop/api/p2p/nf-p2p-peergraphopen">PeerGraphOpen</a>.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_graph_event_data">PEER_GRAPH_EVENT_DATA</a>