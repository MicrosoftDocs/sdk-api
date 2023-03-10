---
UID: NS:p2p.peer_endpoint_tag
title: PEER_ENDPOINT (p2p.h)
description: The PEER_ENDPOINT structure contains the address and friendly name of a peer endpoint.
helpviewer_keywords: ["*PPEER_ENDPOINT","PCPEER_ENDPOINT","PCPEER_ENDPOINT structure pointer [Peer Networking]","PEER_ENDPOINT","PEER_ENDPOINT structure [Peer Networking]","PPEER_ENDPOINT","PPEER_ENDPOINT structure pointer [Peer Networking]","p2p.peer_endpoint","p2p/PCPEER_ENDPOINT","p2p/PEER_ENDPOINT","p2p/PPEER_ENDPOINT"]
old-location: p2p\peer_endpoint.htm
tech.root: p2p
ms.assetid: 9687b332-14ed-4023-b8c2-437d75fd0298
ms.date: 12/05/2018
ms.keywords: '*PPEER_ENDPOINT, PCPEER_ENDPOINT, PCPEER_ENDPOINT structure pointer [Peer Networking], PEER_ENDPOINT, PEER_ENDPOINT structure [Peer Networking], PPEER_ENDPOINT, PPEER_ENDPOINT structure pointer [Peer Networking], p2p.peer_endpoint, p2p/PCPEER_ENDPOINT, p2p/PEER_ENDPOINT, p2p/PPEER_ENDPOINT'
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
req.typenames: PEER_ENDPOINT, *PPEER_ENDPOINT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_endpoint_tag
 - p2p/peer_endpoint_tag
 - PPEER_ENDPOINT
 - p2p/PPEER_ENDPOINT
 - PEER_ENDPOINT
 - p2p/PEER_ENDPOINT
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
 - PEER_ENDPOINT
---

# PEER_ENDPOINT structure


## -description

The <b>PEER_ENDPOINT</b> structure contains the address and friendly name of a peer endpoint.

## -struct-fields

### -field address

<a href="/windows/desktop/api/p2p/ns-p2p-peer_address">PEER_ADDRESS</a> structure that contains the IPv6 network address of the endpoint.

### -field pwzEndpointName

Zero-terminated Unicode string that contains the specific displayable name of the endpoint.

## -remarks

A peer "endpoint" describes a contact's presence location — the unique network address configuration that describes the currently available instance of the contact within the peer collaboration network. A single contact can be available at multiple endpoints within the peer collaboration network.

A peer watching a contact can query any of the endpoints associated with that contact for specific peer presence, application, or object updates.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_address">PEER_ADDRESS</a>



<a href="/windows/desktop/P2PSdk/collaboration-api-structures">Peer Collaboration API Structures</a>