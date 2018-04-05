---
UID: NS:p2p.peer_event_synchronized_data_tag
title: peer_event_synchronized_data_tag
author: windows-driver-content
description: The PEER_EVENT_SYNCHRONIZED_DATA is pointed to by a PEER_GRAPH_EVENT_DATA structure's union if a PEER_GRAPH_EVENT_RECORD_CHANGE or PEER_GROUP_EVENT_RECORD_CHANGE event is triggered.
old-location: p2p\peer_event_synchronized_data.htm
old-project: P2PSdk
ms.assetid: ae7dc220-a827-4671-97b3-1ac039ab3e08
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "*PPEER_EVENT_SYNCHRONIZED_DATA, PEER_EVENT_SYNCHRONIZED_DATA, PEER_EVENT_SYNCHRONIZED_DATA structure [Peer Networking], PPEER_EVENT_SYNCHRONIZED_DATA, PPEER_EVENT_SYNCHRONIZED_DATA structure pointer [Peer Networking], p2p.peer_event_synchronized_data, p2p/PPEER_EVENT_SYNCHRONIZED_DATA, p2p/peer_event_synchronized_data_tag, peer_event_synchronized_data_tag"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: PEER_EVENT_SYNCHRONIZED_DATA, *PPEER_EVENT_SYNCHRONIZED_DATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	P2P.h
api_name:
-	PEER_EVENT_SYNCHRONIZED_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# peer_event_synchronized_data_tag structure


## -description


The <b>PEER_EVENT_SYNCHRONIZED_DATA</b> is pointed to by a <a href="https://msdn.microsoft.com/a052bff8-e90c-4ff7-8362-edb94b130f38">PEER_GRAPH_EVENT_DATA</a> structure's union if a PEER_GRAPH_EVENT_RECORD_CHANGE or  PEER_GROUP_EVENT_RECORD_CHANGE event is triggered. The <b>PEER_EVENT_SYNCHRONIZED_DATA</b> structure indicates the type of record that has been synchronized.


## -struct-fields




### -field dwSize

Specifies the size of the structure.


### -field recordType

Specifies the type of record that is being synchronized.


## -remarks



This event only occurs if an application has specified a record synchronization precedence in a previous call to <a href="https://msdn.microsoft.com/a34656f1-3e29-4bcb-a8a7-0eed19368184">PeerGraphOpen</a>.




## -see-also




<a href="https://msdn.microsoft.com/a052bff8-e90c-4ff7-8362-edb94b130f38">PEER_GRAPH_EVENT_DATA</a>
 

 

