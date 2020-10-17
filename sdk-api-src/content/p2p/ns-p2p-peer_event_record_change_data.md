---
UID: NS:p2p.peer_event_record_change_data_tag
title: PEER_EVENT_RECORD_CHANGE_DATA (p2p.h)
description: Points to the PEER_EVENT_RECORD_CHANGE_DATA structure if one of the following peer events is triggered.
helpviewer_keywords: ["*PPEER_EVENT_RECORD_CHANGE_DATA","PEER_EVENT_RECORD_CHANGE_DATA","PEER_EVENT_RECORD_CHANGE_DATA structure [Peer Networking]","PPEER_EVENT_RECORD_CHANGE_DATA","PPEER_EVENT_RECORD_CHANGE_DATA structure pointer [Peer Networking]","p2p.peer_event_record_change_data","p2p/PPEER_EVENT_RECORD_CHANGE_DATA","p2p/peer_event_record_change_data_tag"]
old-location: p2p\peer_event_record_change_data.htm
tech.root: p2p
ms.assetid: 01404fff-3488-43aa-bc59-3e08ff925ea5
ms.date: 12/05/2018
ms.keywords: '*PPEER_EVENT_RECORD_CHANGE_DATA, PEER_EVENT_RECORD_CHANGE_DATA, PEER_EVENT_RECORD_CHANGE_DATA structure [Peer Networking], PPEER_EVENT_RECORD_CHANGE_DATA, PPEER_EVENT_RECORD_CHANGE_DATA structure pointer [Peer Networking], p2p.peer_event_record_change_data, p2p/PPEER_EVENT_RECORD_CHANGE_DATA, p2p/peer_event_record_change_data_tag'
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
req.typenames: PEER_EVENT_RECORD_CHANGE_DATA, *PPEER_EVENT_RECORD_CHANGE_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_event_record_change_data_tag
 - p2p/peer_event_record_change_data_tag
 - PPEER_EVENT_RECORD_CHANGE_DATA
 - p2p/PPEER_EVENT_RECORD_CHANGE_DATA
 - PEER_EVENT_RECORD_CHANGE_DATA
 - p2p/PEER_EVENT_RECORD_CHANGE_DATA
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
 - PEER_EVENT_RECORD_CHANGE_DATA
---

# PEER_EVENT_RECORD_CHANGE_DATA structure


## -description

The [PEER_GROUP_EVENT_DATA](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1) structure points to the <b>PEER_EVENT_RECORD_CHANGE_DATA</b> structure if one of the following peer events is triggered:
<ul>
<li><b>PEER_GRAPH_EVENT_RECORD_CHANGE</b></li>
<li><b>PEER_GROUP_EVENT_RECORD_CHANGE</b></li>
</ul> The <b>PEER_EVENT_RECORD_CHANGE_DATA</b> structure contains updated information that an application requests for data  changes  to a record or record type.

## -struct-fields

### -field dwSize

Specifies the size of a structure.

### -field changeType

Specifies the type of change to a record or record type.

### -field recordId

Specifies the unique  ID of a changed record.

### -field recordType

Specifies the unique  record type of a changed record.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_graph_event_data">PEER_GRAPH_EVENT_DATA</a>



[PEER_GROUP_EVENT_DATA](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1)



<a href="/windows/desktop/api/p2p/ne-p2p-peer_record_change_type">PEER_RECORD_CHANGE_TYPE</a>