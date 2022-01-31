---
UID: NE:p2p.peer_group_event_type_tag
title: PEER_GROUP_EVENT_TYPE (p2p.h)
description: The PEER_GROUP_EVENT_TYPE enumeration contains the specific peer event types that can occur within a peer group.
helpviewer_keywords: ["PEER_GROUP_EVENT_CONNECTION_FAILED","PEER_GROUP_EVENT_DIRECT_CONNECTION","PEER_GROUP_EVENT_INCOMING_DATA","PEER_GROUP_EVENT_MEMBER_CHANGED","PEER_GROUP_EVENT_NEIGHBOR_CONNECTION","PEER_GROUP_EVENT_PROPERTY_CHANGED","PEER_GROUP_EVENT_RECORD_CHANGED","PEER_GROUP_EVENT_STATUS_CHANGED","PEER_GROUP_EVENT_TYPE","PEER_GROUP_EVENT_TYPE enumeration [Peer Networking]","p2p.peer_group_event_type","p2p/PEER_GROUP_EVENT_CONNECTION_FAILED","p2p/PEER_GROUP_EVENT_DIRECT_CONNECTION","p2p/PEER_GROUP_EVENT_INCOMING_DATA","p2p/PEER_GROUP_EVENT_MEMBER_CHANGED","p2p/PEER_GROUP_EVENT_NEIGHBOR_CONNECTION","p2p/PEER_GROUP_EVENT_PROPERTY_CHANGED","p2p/PEER_GROUP_EVENT_RECORD_CHANGED","p2p/PEER_GROUP_EVENT_STATUS_CHANGED","p2p/PEER_GROUP_EVENT_TYPE"]
old-location: p2p\peer_group_event_type.htm
tech.root: p2p
ms.assetid: 9c28eb24-f158-4313-9a7c-0f271013d03a
ms.date: 12/05/2018
ms.keywords: PEER_GROUP_EVENT_CONNECTION_FAILED, PEER_GROUP_EVENT_DIRECT_CONNECTION, PEER_GROUP_EVENT_INCOMING_DATA, PEER_GROUP_EVENT_MEMBER_CHANGED, PEER_GROUP_EVENT_NEIGHBOR_CONNECTION, PEER_GROUP_EVENT_PROPERTY_CHANGED, PEER_GROUP_EVENT_RECORD_CHANGED, PEER_GROUP_EVENT_STATUS_CHANGED, PEER_GROUP_EVENT_TYPE, PEER_GROUP_EVENT_TYPE enumeration [Peer Networking], p2p.peer_group_event_type, p2p/PEER_GROUP_EVENT_CONNECTION_FAILED, p2p/PEER_GROUP_EVENT_DIRECT_CONNECTION, p2p/PEER_GROUP_EVENT_INCOMING_DATA, p2p/PEER_GROUP_EVENT_MEMBER_CHANGED, p2p/PEER_GROUP_EVENT_NEIGHBOR_CONNECTION, p2p/PEER_GROUP_EVENT_PROPERTY_CHANGED, p2p/PEER_GROUP_EVENT_RECORD_CHANGED, p2p/PEER_GROUP_EVENT_STATUS_CHANGED, p2p/PEER_GROUP_EVENT_TYPE
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
req.typenames: PEER_GROUP_EVENT_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_group_event_type_tag
 - p2p/peer_group_event_type_tag
 - PEER_GROUP_EVENT_TYPE
 - p2p/PEER_GROUP_EVENT_TYPE
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
 - PEER_GROUP_EVENT_TYPE
---

# PEER_GROUP_EVENT_TYPE enumeration


## -description

The <b>PEER_GROUP_EVENT_TYPE</b> enumeration contains the specific peer event types that can occur within a peer group.

## -enum-fields

### -field PEER_GROUP_EVENT_STATUS_CHANGED:1

The status of the group has changed. This peer event is fired when one of the flags listed in the <a href="/windows/desktop/api/p2p/ne-p2p-peer_group_status">PEER_GROUP_STATUS</a> enumeration are set or changed for the group.

### -field PEER_GROUP_EVENT_PROPERTY_CHANGED:2

A member in the [PEER_GROUP_EVENT_DATA](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1) to retrieve.

### -field PEER_GROUP_EVENT_RECORD_CHANGED:3

A group record has changed. Information on this change is provided in the [PEER_GROUP_EVENT_DATA](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1).

### -field PEER_GROUP_EVENT_DIRECT_CONNECTION:4

The status of a direct connection has changed. Information on this change is provided in the [PEER_GROUP_EVENT_DATA](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1).

### -field PEER_GROUP_EVENT_NEIGHBOR_CONNECTION:5

The status of a neighbor connection has changed. Information on this change is provided in the [PEER_GROUP_EVENT_DATA](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1).

### -field PEER_GROUP_EVENT_INCOMING_DATA:6

Incoming direct connection data from a member is detected. Information on this peer event is provided in the [PEER_GROUP_EVENT_DATA](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1).

### -field PEER_GROUP_EVENT_MEMBER_CHANGED:8

The status of a member has changed. Information on this change is provided in the [PEER_GROUP_EVENT_DATA](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1).

### -field PEER_GROUP_EVENT_CONNECTION_FAILED:10

The connection to the peer group has failed. No data is provided when this peer event is raised. This event is also raised if no members are online in a group you are attempting to connect to for the first time.

### -field PEER_GROUP_EVENT_AUTHENTICATION_FAILED:11

## -see-also

[PEER_GROUP_EVENT_DATA](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1)



<a href="/windows/desktop/api/p2p/ns-p2p-peer_group_event_registration">PEER_GROUP_EVENT_REGISTRATION</a>
