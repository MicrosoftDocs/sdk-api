---
UID: NE:p2p.peer_group_event_type_tag
title: PEER_GROUP_EVENT_TYPE (p2p.h)
author: windows-sdk-content
description: The PEER_GROUP_EVENT_TYPE enumeration contains the specific peer event types that can occur within a peer group.
old-location: p2p\peer_group_event_type.htm
tech.root: P2PSdk
ms.assetid: 9c28eb24-f158-4313-9a7c-0f271013d03a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PEER_GROUP_EVENT_CONNECTION_FAILED, PEER_GROUP_EVENT_DIRECT_CONNECTION, PEER_GROUP_EVENT_INCOMING_DATA, PEER_GROUP_EVENT_MEMBER_CHANGED, PEER_GROUP_EVENT_NEIGHBOR_CONNECTION, PEER_GROUP_EVENT_PROPERTY_CHANGED, PEER_GROUP_EVENT_RECORD_CHANGED, PEER_GROUP_EVENT_STATUS_CHANGED, PEER_GROUP_EVENT_TYPE, PEER_GROUP_EVENT_TYPE enumeration [Peer Networking], p2p.peer_group_event_type, p2p/PEER_GROUP_EVENT_CONNECTION_FAILED, p2p/PEER_GROUP_EVENT_DIRECT_CONNECTION, p2p/PEER_GROUP_EVENT_INCOMING_DATA, p2p/PEER_GROUP_EVENT_MEMBER_CHANGED, p2p/PEER_GROUP_EVENT_NEIGHBOR_CONNECTION, p2p/PEER_GROUP_EVENT_PROPERTY_CHANGED, p2p/PEER_GROUP_EVENT_RECORD_CHANGED, p2p/PEER_GROUP_EVENT_STATUS_CHANGED, p2p/PEER_GROUP_EVENT_TYPE
ms.topic: enum
f1_keywords: 
 - "p2p/PEER_GROUP_EVENT_TYPE"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - P2P.h
api_name:
 - PEER_GROUP_EVENT_TYPE
targetos: Windows
req.typenames: PEER_GROUP_EVENT_TYPE
req.redist: 
ms.custom: 19H1
---

# PEER_GROUP_EVENT_TYPE enumeration


## -description


The <b>PEER_GROUP_EVENT_TYPE</b> enumeration contains the specific peer event types that can occur within a peer group.


## -enum-fields




### -field PEER_GROUP_EVENT_STATUS_CHANGED

The status of the group has changed. This peer event is fired when one of the flags listed in the <a href="https://docs.microsoft.com/windows/desktop/api/p2p/ne-p2p-peer_group_status">PEER_GROUP_STATUS</a> enumeration are set or changed for the group.


### -field PEER_GROUP_EVENT_PROPERTY_CHANGED

A member in the <a href="https://docs.microsoft.com/windows/desktop/api/p2p/ns-p2p-peer_group_properties">PEER_GROUP_PROPERTIES</a> structure has changed.   The application already has the change and must use <a href="https://docs.microsoft.com/windows/desktop/api/p2p/nf-p2p-peergroupgetproperties">PeerGroupGetProperties</a> to get the updated structure. This peer event does not have associated data present in <a href="https://docs.microsoft.com/windows/desktop/api/p2p/ns-p2p-peer_group_event_data_tag">PEER_GROUP_EVENT_DATA</a> to retrieve.


### -field PEER_GROUP_EVENT_RECORD_CHANGED

A group record has changed. Information on this change is provided in the <b>recordChangeData</b> member of <a href="https://docs.microsoft.com/windows/desktop/api/p2p/ns-p2p-peer_group_event_data_tag">PEER_GROUP_EVENT_DATA</a>.


### -field PEER_GROUP_EVENT_DIRECT_CONNECTION

The status of a direct connection has changed. Information on this change is provided in the <b>connectionChangeData</b> member of <a href="https://docs.microsoft.com/windows/desktop/api/p2p/ns-p2p-peer_group_event_data_tag">PEER_GROUP_EVENT_DATA</a>.


### -field PEER_GROUP_EVENT_NEIGHBOR_CONNECTION

The status of a neighbor connection has changed. Information on this change is provided in the <b>connectionChangeData</b>  member of <a href="https://docs.microsoft.com/windows/desktop/api/p2p/ns-p2p-peer_group_event_data_tag">PEER_GROUP_EVENT_DATA</a>.


### -field PEER_GROUP_EVENT_INCOMING_DATA

Incoming direct connection data from a member is detected. Information on this peer event is provided in the <b>incomingData</b>  member of <a href="https://docs.microsoft.com/windows/desktop/api/p2p/ns-p2p-peer_group_event_data_tag">PEER_GROUP_EVENT_DATA</a>.


### -field PEER_GROUP_EVENT_MEMBER_CHANGED

The status of a member has changed. Information on this change is provided in the <b>memberChangeData</b>  member of <a href="https://docs.microsoft.com/windows/desktop/api/p2p/ns-p2p-peer_group_event_data_tag">PEER_GROUP_EVENT_DATA</a>.


### -field PEER_GROUP_EVENT_CONNECTION_FAILED

The connection to the peer group has failed. No data is provided when this peer event is raised. This event is also raised if no members are online in a group you are attempting to connect to for the first time. 



### -field PEER_GROUP_EVENT_AUTHENTICATION_FAILED




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/p2p/ns-p2p-peer_group_event_data_tag">PEER_GROUP_EVENT_DATA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/p2p/ns-p2p-peer_group_event_registration">PEER_GROUP_EVENT_REGISTRATION</a>
 

 

