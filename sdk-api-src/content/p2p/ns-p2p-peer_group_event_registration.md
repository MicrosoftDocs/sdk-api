---
UID: NS:p2p.peer_group_event_registration_tag
title: PEER_GROUP_EVENT_REGISTRATION (p2p.h)
description: The PEER_GROUP_EVENT_REGISTRATION structure defines the particular peer group event a member can register for.
helpviewer_keywords: ["*PPEER_GROUP_EVENT_REGISTRATION","PEER_GROUP_EVENT_REGISTRATION","PEER_GROUP_EVENT_REGISTRATION structure [Peer Networking]","PPEER_GROUP_EVENT_REGISTRATION","PPEER_GROUP_EVENT_REGISTRATION structure pointer [Peer Networking]","p2p.peer_group_event_registration","p2p/PPEER_GROUP_EVENT_REGISTRATION","p2p/peer_group_event_registration_tag"]
old-location: p2p\peer_group_event_registration.htm
tech.root: p2p
ms.assetid: 9c9c82c3-b02a-49c2-9a8f-eb355ded8480
ms.date: 12/05/2018
ms.keywords: '*PPEER_GROUP_EVENT_REGISTRATION, PEER_GROUP_EVENT_REGISTRATION, PEER_GROUP_EVENT_REGISTRATION structure [Peer Networking], PPEER_GROUP_EVENT_REGISTRATION, PPEER_GROUP_EVENT_REGISTRATION structure pointer [Peer Networking], p2p.peer_group_event_registration, p2p/PPEER_GROUP_EVENT_REGISTRATION, p2p/peer_group_event_registration_tag'
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
req.typenames: PEER_GROUP_EVENT_REGISTRATION, *PPEER_GROUP_EVENT_REGISTRATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_group_event_registration_tag
 - p2p/peer_group_event_registration_tag
 - PPEER_GROUP_EVENT_REGISTRATION
 - p2p/PPEER_GROUP_EVENT_REGISTRATION
 - PEER_GROUP_EVENT_REGISTRATION
 - p2p/PEER_GROUP_EVENT_REGISTRATION
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
 - PEER_GROUP_EVENT_REGISTRATION
---

# PEER_GROUP_EVENT_REGISTRATION structure


## -description

The <b>PEER_GROUP_EVENT_REGISTRATION</b> structure defines the particular peer group event a member can register for.

## -struct-fields

### -field eventType

<a href="/windows/desktop/api/p2p/ne-p2p-peer_group_event_type">PEER_GROUP_EVENT_TYPE</a> that specifies the peer group event type to register for.

### -field pType

GUID value that identifies the type of record or data message that  raises an event of the type specified by <b>eventType</b>. For example, if the peer wishes to be notified about all changes to a specific record type,  the GUID that corresponds to this record type must be supplied in this field and PEER_GROUP_RECORD_CHANGED must be in <b>eventType</b>.

This member is only populated (not NULL) when <b>eventType</b> is either PEER_GROUP_EVENT_RECORD_CHANGED or PEER_GROUP_EVENT_INCOMING_DATA.

## -see-also

<a href="/windows/desktop/api/p2p/ne-p2p-peer_group_event_type">PEER_GROUP_EVENT_TYPE</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupregisterevent">PeerGroupRegisterEvent</a>