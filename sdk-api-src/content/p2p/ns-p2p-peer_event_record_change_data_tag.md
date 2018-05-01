---
UID: NS:p2p.peer_event_record_change_data_tag
title: peer_event_record_change_data_tag
author: windows-driver-content
description: Points to the PEER_EVENT_RECORD_CHANGE_DATA structure if one of the following peer events is triggered.
old-location: p2p\peer_event_record_change_data.htm
old-project: P2PSdk
ms.assetid: 01404fff-3488-43aa-bc59-3e08ff925ea5
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: "*PPEER_EVENT_RECORD_CHANGE_DATA, PEER_EVENT_RECORD_CHANGE_DATA, PEER_EVENT_RECORD_CHANGE_DATA structure [Peer Networking], PPEER_EVENT_RECORD_CHANGE_DATA, PPEER_EVENT_RECORD_CHANGE_DATA structure pointer [Peer Networking], p2p.peer_event_record_change_data, p2p/PPEER_EVENT_RECORD_CHANGE_DATA, p2p/peer_event_record_change_data_tag, peer_event_record_change_data_tag"
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
req.typenames: PEER_EVENT_RECORD_CHANGE_DATA, *PPEER_EVENT_RECORD_CHANGE_DATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	P2P.h
api_name:
-	PEER_EVENT_RECORD_CHANGE_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# peer_event_record_change_data_tag structure


## -description


The <a href="https://msdn.microsoft.com/a052bff8-e90c-4ff7-8362-edb94b130f38">PEER_GRAPH_EVENT_DATA</a> or <a href="https://msdn.microsoft.com/5cdae832-e6a7-481c-9784-1c1c07d689dd">PEER_GROUP_EVENT_DATA</a> structure points to the <b>PEER_EVENT_RECORD_CHANGE_DATA</b> structure if one of the following peer events is triggered:
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




<a href="https://msdn.microsoft.com/a052bff8-e90c-4ff7-8362-edb94b130f38">PEER_GRAPH_EVENT_DATA</a>



<a href="https://msdn.microsoft.com/5cdae832-e6a7-481c-9784-1c1c07d689dd">PEER_GROUP_EVENT_DATA</a>



<a href="https://msdn.microsoft.com/d2451b45-eb42-4401-ab1d-505a41e25822">PEER_RECORD_CHANGE_TYPE</a>
 

 

