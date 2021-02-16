---
UID: NS:p2p.peer_event_request_status_changed_data_tag
title: PEER_EVENT_REQUEST_STATUS_CHANGED_DATA (p2p.h)
description: The PEER_EVENT_REQUEST_STATUS_CHANGED_DATA structure contains information returned when a PEER_EVENT_REQUEST_STATUS_CHANGED event is raised on a peer participating in a peer collaboration network.
helpviewer_keywords: ["*PPEER_EVENT_REQUEST_STATUS_CHANGED_DATA","PEER_EVENT_REQUEST_STATUS_CHANGED_DATA","PEER_EVENT_REQUEST_STATUS_CHANGED_DATA structure [Peer Networking]","PPEER_EVENT_REQUEST_STATUS_CHANGED_DATA","PPEER_EVENT_REQUEST_STATUS_CHANGED_DATA structure pointer [Peer Networking]","p2p.peer_event_request_status_changed_data","p2p/PEER_EVENT_REQUEST_STATUS_CHANGED_DATA","p2p/PPEER_EVENT_REQUEST_STATUS_CHANGED_DATA"]
old-location: p2p\peer_event_request_status_changed_data.htm
tech.root: p2p
ms.assetid: 88bcf892-5591-49a0-bb00-090f4d5f2f79
ms.date: 12/05/2018
ms.keywords: '*PPEER_EVENT_REQUEST_STATUS_CHANGED_DATA, PEER_EVENT_REQUEST_STATUS_CHANGED_DATA, PEER_EVENT_REQUEST_STATUS_CHANGED_DATA structure [Peer Networking], PPEER_EVENT_REQUEST_STATUS_CHANGED_DATA, PPEER_EVENT_REQUEST_STATUS_CHANGED_DATA structure pointer [Peer Networking], p2p.peer_event_request_status_changed_data, p2p/PEER_EVENT_REQUEST_STATUS_CHANGED_DATA, p2p/PPEER_EVENT_REQUEST_STATUS_CHANGED_DATA'
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
req.typenames: PEER_EVENT_REQUEST_STATUS_CHANGED_DATA, *PPEER_EVENT_REQUEST_STATUS_CHANGED_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_event_request_status_changed_data_tag
 - p2p/peer_event_request_status_changed_data_tag
 - PPEER_EVENT_REQUEST_STATUS_CHANGED_DATA
 - p2p/PPEER_EVENT_REQUEST_STATUS_CHANGED_DATA
 - PEER_EVENT_REQUEST_STATUS_CHANGED_DATA
 - p2p/PEER_EVENT_REQUEST_STATUS_CHANGED_DATA
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
 - PEER_EVENT_REQUEST_STATUS_CHANGED_DATA
---

# PEER_EVENT_REQUEST_STATUS_CHANGED_DATA structure


## -description

The <b>PEER_EVENT_REQUEST_STATUS_CHANGED_DATA</b> structure contains information returned when a PEER_EVENT_REQUEST_STATUS_CHANGED event is raised on a peer participating in a peer collaboration network.

## -struct-fields

### -field pEndpoint

Pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_endpoint">PEER_ENDPOINT</a> structure that contains the peer endpoint information for the contact whose change in request status raised the event.

### -field hrChange

HRESULT value that indicates the change in request status that occurred.

## -remarks

This event is raised when the infrastructure  finishes processing the request for <a href="/windows/desktop/api/p2p/nf-p2p-peercollabrefreshendpointdata">PeerCollabRefreshEndpointData</a> or <a href="/windows/desktop/api/p2p/nf-p2p-peercollabsubscribeendpointdata">PeerCollabSubscribeEndpointData</a>. If the  process fails <b>hrChange</b> value will most typically be PEER_E_CONNECTION_FAILED.

## -see-also

<a href="/windows/desktop/api/p2p/ne-p2p-peer_change_type">PEER_CHANGE_TYPE</a>



<a href="/windows/desktop/api/p2p/ns-p2p-peer_endpoint">PEER_ENDPOINT</a>



<a href="/windows/desktop/P2PSdk/collaboration-api-structures">Peer Collaboration API Structures</a>