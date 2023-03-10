---
UID: NE:p2p.peer_member_change_type_tag
title: PEER_MEMBER_CHANGE_TYPE (p2p.h)
description: The PEER_MEMBER_CHANGE_TYPE enumeration defines the set of possible peer group membership and presence states for a peer.
helpviewer_keywords: ["PEER_MEMBER_CHANGE_TYPE","PEER_MEMBER_CHANGE_TYPE enumeration [Peer Networking]","PEER_MEMBER_CONNECTED","PEER_MEMBER_DISCONNECTED","PEER_MEMBER_JOINED","PEER_MEMBER_LEFT","PEER_MEMBER_UPDATED","p2p.peer_member_change_type","p2p/PEER_MEMBER_CHANGE_TYPE","p2p/PEER_MEMBER_CONNECTED","p2p/PEER_MEMBER_DISCONNECTED","p2p/PEER_MEMBER_JOINED","p2p/PEER_MEMBER_LEFT","p2p/PEER_MEMBER_UPDATED"]
old-location: p2p\peer_member_change_type.htm
tech.root: p2p
ms.assetid: ecebec4f-1dc6-481c-a2d4-cf0043729a8c
ms.date: 12/05/2018
ms.keywords: PEER_MEMBER_CHANGE_TYPE, PEER_MEMBER_CHANGE_TYPE enumeration [Peer Networking], PEER_MEMBER_CONNECTED, PEER_MEMBER_DISCONNECTED, PEER_MEMBER_JOINED, PEER_MEMBER_LEFT, PEER_MEMBER_UPDATED, p2p.peer_member_change_type, p2p/PEER_MEMBER_CHANGE_TYPE, p2p/PEER_MEMBER_CONNECTED, p2p/PEER_MEMBER_DISCONNECTED, p2p/PEER_MEMBER_JOINED, p2p/PEER_MEMBER_LEFT, p2p/PEER_MEMBER_UPDATED
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
req.typenames: PEER_MEMBER_CHANGE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_member_change_type_tag
 - p2p/peer_member_change_type_tag
 - PEER_MEMBER_CHANGE_TYPE
 - p2p/PEER_MEMBER_CHANGE_TYPE
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
 - PEER_MEMBER_CHANGE_TYPE
---

# PEER_MEMBER_CHANGE_TYPE enumeration


## -description

The <b>PEER_MEMBER_CHANGE_TYPE</b> enumeration defines the set of possible peer group membership and presence states for a peer.

## -enum-fields

### -field PEER_MEMBER_CONNECTED:1

A member is connected to a peer group.

### -field PEER_MEMBER_DISCONNECTED:2

A member is disconnected from a peer group.

### -field PEER_MEMBER_UPDATED:3

A member has updated information (for example, a new address) within a peer group.

### -field PEER_MEMBER_JOINED:4

New membership information is published for a group member. The peer name of a peer group member is obtained from the <b>pwzIdentity</b> field of the <a href="/windows/desktop/api/p2p/ns-p2p-peer_event_member_change_data">PEER_EVENT_MEMBER_CHANGE_DATA</a>  structure. New membership information is published in one of the following three scenarios: 

<ul>
<li>An administrator calls <a href="/windows/desktop/api/p2p/nf-p2p-peergroupissuecredentials">PeerGroupIssueCredentials</a> with the PEER_GROUP_STORE_CREDENTIALS flag set.</li>
<li>A user connects to a peer group for the first time, and the PEER_MEMBER_DATA_OPTIONAL flag is not set.</li>
<li>A peer group member performs an operation (for example, issuing an invitation or credentials, or publishing a record), but membership information for the peer group member does not exist in the group.</li>
</ul>

### -field PEER_MEMBER_LEFT:5

This peer event does not exist in the Peer Grouping Infrastructure v1.0, and must not be used.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_event_member_change_data">PEER_EVENT_MEMBER_CHANGE_DATA</a>
