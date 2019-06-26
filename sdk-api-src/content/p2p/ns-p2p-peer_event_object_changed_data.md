---
UID: NS:p2p.peer_event_object_changed_data_tag
title: PEER_EVENT_OBJECT_CHANGED_DATA (p2p.h)
author: windows-sdk-content
description: The PEER_EVENT_OBJECT_CHANGED_DATA structure contains information returned when a PEER_EVENT_ENDPOINT_OBJECT_CHANGED or PEER_EVENT_MY_OBJECT_CHANGED event is raised on a peer participating in a peer collaboration network.
old-location: p2p\peer_event_object_changed_data.htm
tech.root: P2PSdk
ms.assetid: bba6a282-7ccd-45b2-a74c-3258449b990e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PPEER_EVENT_OBJECT_CHANGED_DATA, PEER_EVENT_OBJECT_CHANGED_DATA, PEER_EVENT_OBJECT_CHANGED_DATA structure [Peer Networking], PPEER_EVENT_OBJECT_CHANGED_DATA, PPEER_EVENT_OBJECT_CHANGED_DATA structure pointer [Peer Networking], p2p.peer_event_object_changed_data, p2p/PEER_EVENT_OBJECT_CHANGED_DATA, p2p/PPEER_EVENT_OBJECT_CHANGED_DATA"
ms.topic: struct
f1_keywords: 
 - "p2p/PEER_EVENT_OBJECT_CHANGED_DATA"
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
 - PEER_EVENT_OBJECT_CHANGED_DATA
product: Windows
targetos: Windows
req.typenames: PEER_EVENT_OBJECT_CHANGED_DATA, *PPEER_EVENT_OBJECT_CHANGED_DATA
req.redist: 
ms.custom: 19H1
---

# PEER_EVENT_OBJECT_CHANGED_DATA structure


## -description


The <b>PEER_EVENT_OBJECT_CHANGED_DATA</b> structure contains information returned when a PEER_EVENT_ENDPOINT_OBJECT_CHANGED or PEER_EVENT_MY_OBJECT_CHANGED event is raised on a peer participating in a peer collaboration network.


## -struct-fields




### -field pContact

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/p2p/ns-p2p-peer_contact_tag">PEER_CONTACT</a> structure that contains the peer contact information for the contact whose peer object data changed.


### -field pEndpoint

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/p2p/ns-p2p-peer_endpoint_tag">PEER_ENDPOINT</a> structure that contains the peer endpoint information for the contact whose peer object data changed.


### -field changeType


<a href="https://docs.microsoft.com/windows/desktop/api/p2p/ne-p2p-peer_change_type_tag">PEER_CHANGE_TYPE</a> enumeration value that specifies the type of change that occurred.


### -field pObject

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/p2p/ns-p2p-peer_object_tag">PEER_OBJECT</a> structure that contains the peer object data whose change raised the event. This most commonly occurs when a new peer object is received by the peer.


## -remarks



Peer objects are run-time data items associated with a particular application, such as a picture or avatar, a certificate, or a specific description. Each peer object must be smaller than 16K in size.

Trusted contacts watching this peer object will have a PEER_EVENT_OBJECT_CHANGED event raised on them signaling the peer object's change in status.

The PEER_EVENT_OBJECT_CHANGED event is raised when an object is changed by calling <a href="https://docs.microsoft.com/windows/desktop/api/p2p/nf-p2p-peercollabsetobject">PeerCollabSetObject</a>. If it is the first time the object is set then <b>changeType</b> is set to PEER_CHANGE_ADDED. On subsequent calls of PeerCollabSetObject for the same object ID the <b>changeType</b> is set to PEER_CHANGE_UDPATED.

If <a href="https://docs.microsoft.com/windows/desktop/api/p2p/nf-p2p-peercollabdeleteobject">PeerCollabDeleteObject</a> is called the PEER_CHANGE_DELETED event is raised.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/p2p/ne-p2p-peer_change_type_tag">PEER_CHANGE_TYPE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/p2p/ns-p2p-peer_contact_tag">PEER_CONTACT</a>



<a href="https://docs.microsoft.com/windows/desktop/api/p2p/ns-p2p-peer_endpoint_tag">PEER_ENDPOINT</a>



<a href="https://docs.microsoft.com/windows/desktop/api/p2p/ns-p2p-peer_object_tag">PEER_OBJECT</a>



<a href="https://docs.microsoft.com/windows/desktop/P2PSdk/collaboration-api-structures">Peer Collaboration API Structures</a>
 

 

