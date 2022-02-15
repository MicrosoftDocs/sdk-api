---
UID: NE:p2p.peer_collab_event_type_tag
title: PEER_COLLAB_EVENT_TYPE (p2p.h)
description: The PEER_COLLAB_EVENT_TYPE enumeration defines the set of events that can be raised on a peer by the peer collaboration network event infrastructure.
helpviewer_keywords: ["PEER_COLLAB_EVENT_TYPE","PEER_COLLAB_EVENT_TYPE enumeration [Peer Networking]","PEER_EVENT_ENDPOINT_APPLICATION_CHANGED","PEER_EVENT_ENDPOINT_CHANGED","PEER_EVENT_ENDPOINT_OBJECT_CHANGED","PEER_EVENT_ENDPOINT_PRESENCE_CHANGED","PEER_EVENT_MY_APPLICATION_CHANGED","PEER_EVENT_MY_ENDPOINT_CHANGED","PEER_EVENT_MY_OBJECT_CHANGED","PEER_EVENT_MY_PRESENCE_CHANGED","PEER_EVENT_PEOPLE_NEAR_ME_CHANGED","PEER_EVENT_REQUEST_STATUS_CHANGED","PEER_EVENT_WATCHLIST_CHANGED","p2p.peer_collab_event_type","p2p/PEER_COLLAB_EVENT_TYPE","p2p/PEER_EVENT_ENDPOINT_APPLICATION_CHANGED","p2p/PEER_EVENT_ENDPOINT_CHANGED","p2p/PEER_EVENT_ENDPOINT_OBJECT_CHANGED","p2p/PEER_EVENT_ENDPOINT_PRESENCE_CHANGED","p2p/PEER_EVENT_MY_APPLICATION_CHANGED","p2p/PEER_EVENT_MY_ENDPOINT_CHANGED","p2p/PEER_EVENT_MY_OBJECT_CHANGED","p2p/PEER_EVENT_MY_PRESENCE_CHANGED","p2p/PEER_EVENT_PEOPLE_NEAR_ME_CHANGED","p2p/PEER_EVENT_REQUEST_STATUS_CHANGED","p2p/PEER_EVENT_WATCHLIST_CHANGED"]
old-location: p2p\peer_collab_event_type.htm
tech.root: p2p
ms.assetid: 2266c518-d383-4f37-9494-d57a3f780ced
ms.date: 12/05/2018
ms.keywords: PEER_COLLAB_EVENT_TYPE, PEER_COLLAB_EVENT_TYPE enumeration [Peer Networking], PEER_EVENT_ENDPOINT_APPLICATION_CHANGED, PEER_EVENT_ENDPOINT_CHANGED, PEER_EVENT_ENDPOINT_OBJECT_CHANGED, PEER_EVENT_ENDPOINT_PRESENCE_CHANGED, PEER_EVENT_MY_APPLICATION_CHANGED, PEER_EVENT_MY_ENDPOINT_CHANGED, PEER_EVENT_MY_OBJECT_CHANGED, PEER_EVENT_MY_PRESENCE_CHANGED, PEER_EVENT_PEOPLE_NEAR_ME_CHANGED, PEER_EVENT_REQUEST_STATUS_CHANGED, PEER_EVENT_WATCHLIST_CHANGED, p2p.peer_collab_event_type, p2p/PEER_COLLAB_EVENT_TYPE, p2p/PEER_EVENT_ENDPOINT_APPLICATION_CHANGED, p2p/PEER_EVENT_ENDPOINT_CHANGED, p2p/PEER_EVENT_ENDPOINT_OBJECT_CHANGED, p2p/PEER_EVENT_ENDPOINT_PRESENCE_CHANGED, p2p/PEER_EVENT_MY_APPLICATION_CHANGED, p2p/PEER_EVENT_MY_ENDPOINT_CHANGED, p2p/PEER_EVENT_MY_OBJECT_CHANGED, p2p/PEER_EVENT_MY_PRESENCE_CHANGED, p2p/PEER_EVENT_PEOPLE_NEAR_ME_CHANGED, p2p/PEER_EVENT_REQUEST_STATUS_CHANGED, p2p/PEER_EVENT_WATCHLIST_CHANGED
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
req.typenames: PEER_COLLAB_EVENT_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_collab_event_type_tag
 - p2p/peer_collab_event_type_tag
 - PEER_COLLAB_EVENT_TYPE
 - p2p/PEER_COLLAB_EVENT_TYPE
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
 - PEER_COLLAB_EVENT_TYPE
---

# PEER_COLLAB_EVENT_TYPE enumeration


## -description

The <b>PEER_COLLAB_EVENT_TYPE</b> enumeration defines the set of events that can be raised on a peer by the peer collaboration network event infrastructure.

## -enum-fields

### -field PEER_EVENT_WATCHLIST_CHANGED:1

The peer's list of watched contacts has changed.

### -field PEER_EVENT_ENDPOINT_CHANGED:2

The endpoint has changed.

### -field PEER_EVENT_ENDPOINT_PRESENCE_CHANGED:3

The presence status of an endpoint has changed.

### -field PEER_EVENT_ENDPOINT_APPLICATION_CHANGED:4

The registered application of the endpoint has changed.

### -field PEER_EVENT_ENDPOINT_OBJECT_CHANGED:5

A peer object registered to the endpoint has changed.

### -field PEER_EVENT_MY_ENDPOINT_CHANGED:6

The local peer's endpoint has changed.

### -field PEER_EVENT_MY_PRESENCE_CHANGED:7

The local peer's presence status has changed.

### -field PEER_EVENT_MY_APPLICATION_CHANGED:8

The local peer's registered application has changed.

### -field PEER_EVENT_MY_OBJECT_CHANGED:9

A peer object registered with the local peer has changed.

### -field PEER_EVENT_PEOPLE_NEAR_ME_CHANGED:10

An endpoint in the same subnet as the local peer's endpoint has changed.

### -field PEER_EVENT_REQUEST_STATUS_CHANGED:11

The status of a  request to refresh endpoint data or subscribe to endpoint data has changed.

## -see-also

<a href="/windows/desktop/P2PSdk/collaboration-api-enumerations">Collaboration API Enumerations</a>
