---
UID: NS:p2p.peer_event_people_near_me_changed_data_tag
title: PEER_EVENT_PEOPLE_NEAR_ME_CHANGED_DATA (p2p.h)
description: The PEER_EVENT_PEOPLE_NEAR_ME_CHANGED_DATA structure contains information returned when a PEER_EVENT_PEOPLE_NEAR_ME_CHANGED event is raised on a peer participating in a subnet-specific peer collaboration network.
helpviewer_keywords: ["*PPEER_EVENT_PEOPLE_NEAR_ME_CHANGED_DATA","PEER_EVENT_PEOPLE_NEAR_ME_CHANGED_DATA","PEER_EVENT_PEOPLE_NEAR_ME_CHANGED_DATA structure [Peer Networking]","PPEER_EVENT_PEOPLE_NEAR_ME_CHANGED_DATA","PPEER_EVENT_PEOPLE_NEAR_ME_CHANGED_DATA structure pointer [Peer Networking]","p2p.peer_event_people_near_me_changed_data","p2p/PEER_EVENT_PEOPLE_NEAR_ME_CHANGED_DATA","p2p/PPEER_EVENT_PEOPLE_NEAR_ME_CHANGED_DATA"]
old-location: p2p\peer_event_people_near_me_changed_data.htm
tech.root: p2p
ms.assetid: d983a399-17b1-43ea-a8fb-05b5d75e179a
ms.date: 12/05/2018
ms.keywords: '*PPEER_EVENT_PEOPLE_NEAR_ME_CHANGED_DATA, PEER_EVENT_PEOPLE_NEAR_ME_CHANGED_DATA, PEER_EVENT_PEOPLE_NEAR_ME_CHANGED_DATA structure [Peer Networking], PPEER_EVENT_PEOPLE_NEAR_ME_CHANGED_DATA, PPEER_EVENT_PEOPLE_NEAR_ME_CHANGED_DATA structure pointer [Peer Networking], p2p.peer_event_people_near_me_changed_data, p2p/PEER_EVENT_PEOPLE_NEAR_ME_CHANGED_DATA, p2p/PPEER_EVENT_PEOPLE_NEAR_ME_CHANGED_DATA'
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.typenames: PEER_EVENT_PEOPLE_NEAR_ME_CHANGED_DATA, *PPEER_EVENT_PEOPLE_NEAR_ME_CHANGED_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_event_people_near_me_changed_data_tag
 - p2p/peer_event_people_near_me_changed_data_tag
 - PPEER_EVENT_PEOPLE_NEAR_ME_CHANGED_DATA
 - p2p/PPEER_EVENT_PEOPLE_NEAR_ME_CHANGED_DATA
 - PEER_EVENT_PEOPLE_NEAR_ME_CHANGED_DATA
 - p2p/PEER_EVENT_PEOPLE_NEAR_ME_CHANGED_DATA
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
 - PEER_EVENT_PEOPLE_NEAR_ME_CHANGED_DATA
---

# PEER_EVENT_PEOPLE_NEAR_ME_CHANGED_DATA structure


## -description

The <b>PEER_EVENT_PEOPLE_NEAR_ME_CHANGED_DATA</b> structure contains information returned when a PEER_EVENT_PEOPLE_NEAR_ME_CHANGED event is raised on a peer participating in a subnet-specific peer collaboration network.

## -struct-fields

### -field changeType

<a href="/windows/desktop/api/p2p/ne-p2p-peer_change_type">PEER_CHANGE_TYPE</a> enumeration value that describes the type of change that occurred for a contact available on the local subnet.

### -field pPeopleNearMe

Pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_people_near_me">PEER_PEOPLE_NEAR_ME</a> structure that contains the peer endpoint information for the contact on the subnet that raised the change event.

## -remarks

The information that can be changed in a peer contact include the endpoint's name or its associated IPv6 address. 

 If the <b>changeType</b> is set to PEER_CHANGE_ADDED and <b>pEndpoint</b> is set to <b>NULL</b>, then the local peer has signed in. Otherwise, if <b>changeType</b> is set to PEER_CHANGE_DELETEDimplies the local peer has signed out.

## -see-also

<a href="/windows/desktop/api/p2p/ne-p2p-peer_change_type">PEER_CHANGE_TYPE</a>



<a href="/windows/desktop/api/p2p/ns-p2p-peer_people_near_me">PEER_PEOPLE_NEAR_ME</a>



<a href="/windows/desktop/P2PSdk/collaboration-api-structures">Peer Collaboration API Structures</a>