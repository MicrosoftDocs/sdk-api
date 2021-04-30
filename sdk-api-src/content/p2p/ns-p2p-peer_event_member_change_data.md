---
UID: NS:p2p.peer_event_member_change_data_tag
title: PEER_EVENT_MEMBER_CHANGE_DATA (p2p.h)
description: The PEER_EVENT_MEMBER_CHANGE_DATA structure contains data that describes a change in the status of a peer group member.
helpviewer_keywords: ["*PPEER_EVENT_MEMBER_CHANGE_DATA","PEER_EVENT_MEMBER_CHANGE_DATA","PEER_EVENT_MEMBER_CHANGE_DATA structure [Peer Networking]","PPEER_EVENT_MEMBER_CHANGE_DATA","PPEER_EVENT_MEMBER_CHANGE_DATA structure pointer [Peer Networking]","p2p.peer_event_member_change_data","p2p/PPEER_EVENT_MEMBER_CHANGE_DATA","p2p/peer_event_member_change_data_tag"]
old-location: p2p\peer_event_member_change_data.htm
tech.root: p2p
ms.assetid: 5ba37006-1ded-4996-a190-d789e5cc0755
ms.date: 12/05/2018
ms.keywords: '*PPEER_EVENT_MEMBER_CHANGE_DATA, PEER_EVENT_MEMBER_CHANGE_DATA, PEER_EVENT_MEMBER_CHANGE_DATA structure [Peer Networking], PPEER_EVENT_MEMBER_CHANGE_DATA, PPEER_EVENT_MEMBER_CHANGE_DATA structure pointer [Peer Networking], p2p.peer_event_member_change_data, p2p/PPEER_EVENT_MEMBER_CHANGE_DATA, p2p/peer_event_member_change_data_tag'
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
req.typenames: PEER_EVENT_MEMBER_CHANGE_DATA, *PPEER_EVENT_MEMBER_CHANGE_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_event_member_change_data_tag
 - p2p/peer_event_member_change_data_tag
 - PPEER_EVENT_MEMBER_CHANGE_DATA
 - p2p/PPEER_EVENT_MEMBER_CHANGE_DATA
 - PEER_EVENT_MEMBER_CHANGE_DATA
 - p2p/PEER_EVENT_MEMBER_CHANGE_DATA
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
 - PEER_EVENT_MEMBER_CHANGE_DATA
---

# PEER_EVENT_MEMBER_CHANGE_DATA structure


## -description

The <b>PEER_EVENT_MEMBER_CHANGE_DATA</b> structure contains data that describes a change in the status of a peer group member.

## -struct-fields

### -field dwSize

Contains the size of this structure, in bytes.

### -field changeType

<b>PEER_MEMBER_CHANGE_TYPE</b> enumeration value that specifies the change event that occurred, such as a member joining or leaving.

### -field pwzIdentity

Pointer to a Unicode string that contains the peer name of the peer group member.

## -see-also

[PEER_GROUP_EVENT_DATA](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1)



<a href="/windows/desktop/api/p2p/ns-p2p-peer_group_event_registration">PEER_GROUP_EVENT_REGISTRATION</a>



<a href="/windows/desktop/api/p2p/ne-p2p-peer_member_change_type">PEER_MEMBER_CHANGE_TYPE</a>