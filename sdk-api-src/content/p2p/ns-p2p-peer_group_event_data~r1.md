---
UID: NS:p2p.peer_group_event_data_tag~r1
title: PEER_GROUP_EVENT_DATA
description: The PEER_GROUP_EVENT_DATA structure (p2p.h) contains information about a specific peer group event that has occurred.
ms.date: 08/15/2022
ms.keywords: peer_group_event_data_tag, PEER_GROUP_EVENT_DATA
targetos: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: p2p.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.typenames: PEER_GROUP_EVENT_DATA, *PPEER_GROUP_EVENT_DATA
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - peer_group_event_data_tag
 - p2p/peer_group_event_data_tag
 - PPEER_GROUP_EVENT_DATA
 - p2p/PPEER_GROUP_EVENT_DATA
 - PEER_GROUP_EVENT_DATA
 - p2p/PEER_GROUP_EVENT_DATA
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - p2p.h
api_name:
 - peer_group_event_data_tag
 - PEER_GROUP_EVENT_DATA
---

# PEER_GROUP_EVENT_DATA structure


## -description

The <b>PEER_GROUP_EVENT_DATA</b> structure contains information about a specific peer group event that has occurred.

## -struct-fields

### -field eventType

<a href="/windows/desktop/api/p2p/ne-p2p-peer_group_event_type">PEER_GROUP_EVENT_TYPE</a> enumeration value that specifies  the type of peer group event that occurred. The type of event dictates the subsequent structure chosen from the union; for example, if this value is set to PEER_GROUP_EVENT_INCOMING_DATA, the populated union member is  <b>incomingData</b>.

### -field __unnamed_union_03e8_3

### -field dwStatus

Specifies the <a href="/windows/desktop/api/p2p/ne-p2p-peer_group_status">PEER_GROUP_STATUS</a> flag values that indicate the new status of the peer group. This field is populated  if a PEER_GROUP_EVENT_STATUS_CHANGED event is raised.

### -field incomingData

Specifies the <a href="/windows/desktop/api/p2p/ns-p2p-peer_event_incoming_data">PEER_EVENT_INCOMING_DATA</a> structure that contains information on incoming data from a peer. This structure is populated if a PEER_GROUP_EVENT_INCOMING_DATA  event is raised.

### -field recordChangeData

Specifies the <a href="/windows/desktop/api/p2p/ns-p2p-peer_event_record_change_data">PEER_EVENT_RECORD_CHANGE_DATA</a> structure that contains data that describes a record change. This structure is populated if a PEER_GROUP_EVENT_RECORD_CHANGED event is raised.

### -field connectionChangeData

<a href="/windows/desktop/api/p2p/ns-p2p-peer_event_connection_change_data">PEER_EVENT_CONNECTION_CHANGE_DATA</a> structure that contains information when a direct or neighbor connection has changed. This structure is populated if a  PEER_GROUP_EVENT_DIRECT_CONNECTION or PEER_GROUP_EVENT_NEIGHBOR_CONNECTION event is raised.

### -field memberChangeData

<a href="/windows/desktop/api/p2p/ns-p2p-peer_event_member_change_data">PEER_EVENT_MEMBER_CHANGE_DATA</a> structure that contains data when the status of a peer group member changes. This structure is populated if a PEER_GROUP_EVENT_MEMBER_CHANGED event is raised.

### -field hrConnectionFailedReason

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

## -remarks

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_event_connection_change_data">PEER_EVENT_CONNECTION_CHANGE_DATA</a>

<a href="/windows/desktop/api/p2p/ns-p2p-peer_event_incoming_data">PEER_EVENT_INCOMING_DATA</a>

<a href="/windows/desktop/api/p2p/ns-p2p-peer_event_member_change_data">PEER_EVENT_MEMBER_CHANGE_DATA</a>

<a href="/windows/desktop/api/p2p/ns-p2p-peer_event_record_change_data">PEER_EVENT_RECORD_CHANGE_DATA</a>

<a href="/windows/desktop/api/p2p/ne-p2p-peer_group_event_type">PEER_GROUP_EVENT_TYPE</a>

<a href="/windows/desktop/api/p2p/ne-p2p-peer_group_status">PEER_GROUP_STATUS</a>

<a href="/windows/desktop/api/p2p/nf-p2p-peergroupgeteventdata">PeerGroupGetEventData</a>
