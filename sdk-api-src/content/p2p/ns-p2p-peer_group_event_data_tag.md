---
UID: NS:p2p.peer_group_event_data_tag
title: peer_group_event_data_tag
author: windows-driver-content
description: The PEER_GROUP_EVENT_DATA structure contains information about a specific peer group event that has occurred.
old-location: p2p\peer_group_event_data.htm
old-project: P2PSdk
ms.assetid: 5cdae832-e6a7-481c-9784-1c1c07d689dd
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "*PPEER_GROUP_EVENT_DATA, PEER_E_NOT_AUTHORIZED, PEER_E_NO_MEMBERS_FOUND, PEER_E_NO_MEMBER_CONNECTIONS, PEER_E_UNABLE_TO_LISTEN, PEER_GROUP_EVENT_DATA, PEER_GROUP_EVENT_DATA structure [Peer Networking], PPEER_GROUP_EVENT_DATA, PPEER_GROUP_EVENT_DATA structure pointer [Peer Networking], p2p.peer_group_event_data, p2p/PPEER_GROUP_EVENT_DATA, p2p/peer_group_event_data_tag, peer_group_event_data_tag"
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
req.typenames: PEER_GROUP_EVENT_DATA, *PPEER_GROUP_EVENT_DATA, PEER_GROUP_EVENT_DATA, *PPEER_GROUP_EVENT_DATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	P2P.h
api_name:
-	PEER_GROUP_EVENT_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# peer_group_event_data_tag structure


## -description


The <b>PEER_GROUP_EVENT_DATA</b> structure contains information about a specific peer group event that has occurred. 


## -struct-fields




### -field eventType


<a href="https://msdn.microsoft.com/9c28eb24-f158-4313-9a7c-0f271013d03a">PEER_GROUP_EVENT_TYPE</a> enumeration value that specifies  the type of peer group event that occurred. The type of event dictates the subsequent structure chosen from the union; for example, if this value is set to PEER_GROUP_EVENT_INCOMING_DATA, the populated union member is  <b>incomingData</b>.


#### - connectionChangeData


<a href="https://msdn.microsoft.com/0d73432c-c1e5-4fa9-a812-377b22a47440">PEER_EVENT_CONNECTION_CHANGE_DATA</a> structure that contains information when a direct or neighbor connection has changed. This structure is populated if a  PEER_GROUP_EVENT_DIRECT_CONNECTION or PEER_GROUP_EVENT_NEIGHBOR_CONNECTION event is raised.


#### - dwStatus

Specifies the <a href="https://msdn.microsoft.com/ed3fa9a6-5180-419f-b5d1-02889bbcdd0d">PEER_GROUP_STATUS</a> flag values that indicate the new status of the peer group. This field is populated  if a PEER_GROUP_EVENT_STATUS_CHANGED event is raised.


#### - hrConnectionFailedReason

<b>HRESULT</b> that indicates the type of connection failure that occurred. This value is populated if a PEER_GROUP_EVENT_CONNECTION_FAILED event is raised. This value is one of the following:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PEER_E_NO_MEMBERS_FOUND"></a><a id="peer_e_no_members_found"></a><dl>
<dt><b>PEER_E_NO_MEMBERS_FOUND</b></dt>
</dl>
</td>
<td width="60%">
No  available peers within the peer group were found to connect to.

</td>
</tr>
<tr>
<td width="40%"><a id="PEER_E_NO_MEMBER_CONNECTIONS"></a><a id="peer_e_no_member_connections"></a><dl>
<dt><b>PEER_E_NO_MEMBER_CONNECTIONS</b></dt>
</dl>
</td>
<td width="60%">
No member connections were available.

</td>
</tr>
<tr>
<td width="40%"><a id="PEER_E_UNABLE_TO_LISTEN"></a><a id="peer_e_unable_to_listen"></a><dl>
<dt><b>PEER_E_UNABLE_TO_LISTEN</b></dt>
</dl>
</td>
<td width="60%">
The peer was unable to receive connection data for an unspecified reason.

</td>
</tr>
<tr>
<td width="40%"><a id="PEER_E_NOT_AUTHORIZED"></a><a id="peer_e_not_authorized"></a><dl>
<dt><b>PEER_E_NOT_AUTHORIZED</b></dt>
</dl>
</td>
<td width="60%">
An attempt has been made to perform an unauthorized operation. For example, attempting to join a group with an invalid password.

</td>
</tr>
</table>
 


#### - incomingData

Specifies the <a href="https://msdn.microsoft.com/93104ca5-b3de-492c-965e-3acd12d05ea6">PEER_EVENT_INCOMING_DATA</a> structure that contains information on incoming data from a peer. This structure is populated if a PEER_GROUP_EVENT_INCOMING_DATA  event is raised.


#### - memberChangeData


<a href="https://msdn.microsoft.com/5ba37006-1ded-4996-a190-d789e5cc0755">PEER_EVENT_MEMBER_CHANGE_DATA</a> structure that contains data when the status of a peer group member changes. This structure is populated if a PEER_GROUP_EVENT_MEMBER_CHANGED event is raised.


#### - recordChangeData

Specifies the <a href="https://msdn.microsoft.com/01404fff-3488-43aa-bc59-3e08ff925ea5">PEER_EVENT_RECORD_CHANGE_DATA</a> structure that contains data that describes a record change. This structure is populated if a PEER_GROUP_EVENT_RECORD_CHANGED event is raised.


## -see-also




<a href="https://msdn.microsoft.com/0d73432c-c1e5-4fa9-a812-377b22a47440">PEER_EVENT_CONNECTION_CHANGE_DATA</a>



<a href="https://msdn.microsoft.com/93104ca5-b3de-492c-965e-3acd12d05ea6">PEER_EVENT_INCOMING_DATA</a>



<a href="https://msdn.microsoft.com/5ba37006-1ded-4996-a190-d789e5cc0755">PEER_EVENT_MEMBER_CHANGE_DATA</a>



<a href="https://msdn.microsoft.com/01404fff-3488-43aa-bc59-3e08ff925ea5">PEER_EVENT_RECORD_CHANGE_DATA</a>



<a href="https://msdn.microsoft.com/9c28eb24-f158-4313-9a7c-0f271013d03a">PEER_GROUP_EVENT_TYPE</a>



<a href="https://msdn.microsoft.com/ed3fa9a6-5180-419f-b5d1-02889bbcdd0d">PEER_GROUP_STATUS</a>



<a href="https://msdn.microsoft.com/bc742c09-190d-412e-ae1a-f1350b3748f5">PeerGroupGetEventData</a>
 

 

