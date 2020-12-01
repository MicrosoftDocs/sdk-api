---
UID: NS:p2p.peer_event_application_changed_data_tag
title: PEER_EVENT_APPLICATION_CHANGED_DATA (p2p.h)
description: The PEER_EVENT_APPLICATION_CHANGED_DATA structure contains information returned when a PEER_EVENT_ENDPOINT_APPLICATION_CHANGED or PEER_EVENT_MY_APPLICATION_CHANGED event is raised on a peer participating in a peer collaboration network.
helpviewer_keywords: ["*PPEER_EVENT_APPLICATION_CHANGED_DATA","PEER_EVENT_APPLICATION_CHANGED_DATA","PEER_EVENT_APPLICATION_CHANGED_DATA structure [Peer Networking]","PPEER_EVENT_APPLICATION_CHANGED_DATA","PPEER_EVENT_APPLICATION_CHANGED_DATA structure pointer [Peer Networking]","p2p.peer_event_application_changed_data","p2p/PEER_EVENT_APPLICATION_CHANGED_DATA","p2p/PPEER_EVENT_APPLICATION_CHANGED_DATA"]
old-location: p2p\peer_event_application_changed_data.htm
tech.root: p2p
ms.assetid: f06e9fbd-7655-4d00-8d84-78852a34f016
ms.date: 12/05/2018
ms.keywords: '*PPEER_EVENT_APPLICATION_CHANGED_DATA, PEER_EVENT_APPLICATION_CHANGED_DATA, PEER_EVENT_APPLICATION_CHANGED_DATA structure [Peer Networking], PPEER_EVENT_APPLICATION_CHANGED_DATA, PPEER_EVENT_APPLICATION_CHANGED_DATA structure pointer [Peer Networking], p2p.peer_event_application_changed_data, p2p/PEER_EVENT_APPLICATION_CHANGED_DATA, p2p/PPEER_EVENT_APPLICATION_CHANGED_DATA'
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
req.typenames: PEER_EVENT_APPLICATION_CHANGED_DATA, *PPEER_EVENT_APPLICATION_CHANGED_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_event_application_changed_data_tag
 - p2p/peer_event_application_changed_data_tag
 - PPEER_EVENT_APPLICATION_CHANGED_DATA
 - p2p/PPEER_EVENT_APPLICATION_CHANGED_DATA
 - PEER_EVENT_APPLICATION_CHANGED_DATA
 - p2p/PEER_EVENT_APPLICATION_CHANGED_DATA
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
 - PEER_EVENT_APPLICATION_CHANGED_DATA
---

# PEER_EVENT_APPLICATION_CHANGED_DATA structure


## -description

The <b>PEER_EVENT_APPLICATION_CHANGED_DATA</b> structure contains information returned when a PEER_EVENT_ENDPOINT_APPLICATION_CHANGED or PEER_EVENT_MY_APPLICATION_CHANGED event is raised on a peer participating in a peer collaboration network.

## -struct-fields

### -field pContact

Pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_contact">PEER_CONTACT</a> structure that contains the peer contact information for a contact whose change in application  raised the event.

### -field pEndpoint

Pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_endpoint">PEER_ENDPOINT</a> structure that contains the peer endpoint information for a contact whose change in application information raised the event.

### -field changeType

<a href="/windows/desktop/api/p2p/ne-p2p-peer_change_type">PEER_CHANGE_TYPE</a> enumeration value that specifies the type of application change that occurred.

### -field pApplication

Pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_application">PEER_APPLICATION</a> structure that contains the changed application information.

## -remarks

"Application" is a set of software or software  features available on the peer's endpoint. Commonly, this refers to software packages that support peer networking activities, like games or other collaborative applications.

A peer's application has a GUID representing a single specific application. When an application is registered for a peer, this GUID and the corresponding application can be made available to all trusted contacts of the peer, indicating the activities the peer can participate in. To deregister a peer's application, call <a href="/windows/desktop/api/p2p/nf-p2p-peercollabunregisterapplication">PeerCollabUnregisterApplication</a> with this GUID.

When a new application is registered locally using PeerCollabRegisterApplication or unregistered using PeerCollabUnregisterApplication all peers subscribed to the local peer's presence information receive the PEER_EVENT_ENDPOINT_APPLICATION_CHANGED event. Locally, applications receive the PEER_EVENT_MY_APPLICATION_CHANGED event. 

The <b>current user</b> scope has priority over the <b>all user</b> scope. If the application is registered in both scopes, the event will be fired only if the <b>current user</b> scope is changed.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_application">PEER_APPLICATION</a>



<a href="/windows/desktop/api/p2p/ne-p2p-peer_change_type">PEER_CHANGE_TYPE</a>



<a href="/windows/desktop/api/p2p/ns-p2p-peer_contact">PEER_CONTACT</a>



<a href="/windows/desktop/api/p2p/ns-p2p-peer_endpoint">PEER_ENDPOINT</a>



<a href="/windows/desktop/P2PSdk/collaboration-api-structures">Peer Collaboration API Structures</a>