---
UID: NE:p2p.peer_collab_event_type_tag
title: PEER_COLLAB_EVENT_TYPE
author: windows-sdk-content
description: The PEER_COLLAB_EVENT_TYPE enumeration defines the set of events that can be raised on a peer by the peer collaboration network event infrastructure.
old-location: p2p\peer_collab_event_type.htm
tech.root: P2PSdk
ms.assetid: 2266c518-d383-4f37-9494-d57a3f780ced
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PEER_COLLAB_EVENT_TYPE, PEER_COLLAB_EVENT_TYPE enumeration [Peer Networking], PEER_EVENT_ENDPOINT_APPLICATION_CHANGED, PEER_EVENT_ENDPOINT_CHANGED, PEER_EVENT_ENDPOINT_OBJECT_CHANGED, PEER_EVENT_ENDPOINT_PRESENCE_CHANGED, PEER_EVENT_MY_APPLICATION_CHANGED, PEER_EVENT_MY_ENDPOINT_CHANGED, PEER_EVENT_MY_OBJECT_CHANGED, PEER_EVENT_MY_PRESENCE_CHANGED, PEER_EVENT_PEOPLE_NEAR_ME_CHANGED, PEER_EVENT_REQUEST_STATUS_CHANGED, PEER_EVENT_WATCHLIST_CHANGED, p2p.peer_collab_event_type, p2p/PEER_COLLAB_EVENT_TYPE, p2p/PEER_EVENT_ENDPOINT_APPLICATION_CHANGED, p2p/PEER_EVENT_ENDPOINT_CHANGED, p2p/PEER_EVENT_ENDPOINT_OBJECT_CHANGED, p2p/PEER_EVENT_ENDPOINT_PRESENCE_CHANGED, p2p/PEER_EVENT_MY_APPLICATION_CHANGED, p2p/PEER_EVENT_MY_ENDPOINT_CHANGED, p2p/PEER_EVENT_MY_OBJECT_CHANGED, p2p/PEER_EVENT_MY_PRESENCE_CHANGED, p2p/PEER_EVENT_PEOPLE_NEAR_ME_CHANGED, p2p/PEER_EVENT_REQUEST_STATUS_CHANGED, p2p/PEER_EVENT_WATCHLIST_CHANGED
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - P2P.h
api_name:
 - PEER_COLLAB_EVENT_TYPE
product: Windows
targetos: Windows
req.typenames: PEER_COLLAB_EVENT_TYPE
req.redist: 
---

# PEER_COLLAB_EVENT_TYPE enumeration


## -description


The <b>PEER_COLLAB_EVENT_TYPE</b> enumeration defines the set of events that can be raised on a peer by the peer collaboration network event infrastructure.


## -enum-fields




### -field PEER_EVENT_WATCHLIST_CHANGED

The peer's list of watched contacts has changed.


### -field PEER_EVENT_ENDPOINT_CHANGED

The endpoint has changed.


### -field PEER_EVENT_ENDPOINT_PRESENCE_CHANGED

The presence status of an endpoint has changed.


### -field PEER_EVENT_ENDPOINT_APPLICATION_CHANGED

The registered application of the endpoint has changed.


### -field PEER_EVENT_ENDPOINT_OBJECT_CHANGED

A peer object registered to the endpoint has changed.


### -field PEER_EVENT_MY_ENDPOINT_CHANGED

The local peer's endpoint has changed.


### -field PEER_EVENT_MY_PRESENCE_CHANGED

The local peer's presence status has changed.


### -field PEER_EVENT_MY_APPLICATION_CHANGED

The local peer's registered application has changed.


### -field PEER_EVENT_MY_OBJECT_CHANGED

A peer object registered with the local peer has changed.


### -field PEER_EVENT_PEOPLE_NEAR_ME_CHANGED

An endpoint in the same subnet as the local peer's endpoint has changed.


### -field PEER_EVENT_REQUEST_STATUS_CHANGED

The status of a  request to refresh endpoint data or subscribe to endpoint data has changed.


## -see-also




<a href="https://msdn.microsoft.com/f72e372a-0d23-47f4-8518-1296ec81ce55">Collaboration API Enumerations</a>
 

 

