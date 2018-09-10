---
UID: NS:p2p.peer_event_application_changed_data_tag
title: peer_event_application_changed_data_tag
author: windows-sdk-content
description: The PEER_EVENT_APPLICATION_CHANGED_DATA structure contains information returned when a PEER_EVENT_ENDPOINT_APPLICATION_CHANGED or PEER_EVENT_MY_APPLICATION_CHANGED event is raised on a peer participating in a peer collaboration network.
old-location: p2p\peer_event_application_changed_data.htm
tech.root: p2psdk
ms.assetid: f06e9fbd-7655-4d00-8d84-78852a34f016
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PPEER_EVENT_APPLICATION_CHANGED_DATA, PEER_EVENT_APPLICATION_CHANGED_DATA, PEER_EVENT_APPLICATION_CHANGED_DATA structure [Peer Networking], PPEER_EVENT_APPLICATION_CHANGED_DATA, PPEER_EVENT_APPLICATION_CHANGED_DATA structure pointer [Peer Networking], p2p.peer_event_application_changed_data, p2p/PEER_EVENT_APPLICATION_CHANGED_DATA, p2p/PPEER_EVENT_APPLICATION_CHANGED_DATA, peer_event_application_changed_data_tag"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
 - PEER_EVENT_APPLICATION_CHANGED_DATA
product: Windows
targetos: Windows
req.typenames: PEER_EVENT_APPLICATION_CHANGED_DATA, *PPEER_EVENT_APPLICATION_CHANGED_DATA
req.redist: 
---

# peer_event_application_changed_data_tag structure


## -description


The <b>PEER_EVENT_APPLICATION_CHANGED_DATA</b> structure contains information returned when a PEER_EVENT_ENDPOINT_APPLICATION_CHANGED or PEER_EVENT_MY_APPLICATION_CHANGED event is raised on a peer participating in a peer collaboration network.


## -struct-fields




### -field pContact

Pointer to a <a href="https://msdn.microsoft.com/b84a17fc-35d6-4098-9bb3-18e708541a80">PEER_CONTACT</a> structure that contains the peer contact information for a contact whose change in application  raised the event.


### -field pEndpoint

Pointer to a <a href="https://msdn.microsoft.com/9687b332-14ed-4023-b8c2-437d75fd0298">PEER_ENDPOINT</a> structure that contains the peer endpoint information for a contact whose change in application information raised the event.


### -field changeType


<a href="https://msdn.microsoft.com/ef8f1cc7-e1db-4d6d-9ff6-141746d0787a">PEER_CHANGE_TYPE</a> enumeration value that specifies the type of application change that occurred.


### -field pApplication

Pointer to a <a href="https://msdn.microsoft.com/a219231b-75d0-47d3-8294-f1cc25b43d27">PEER_APPLICATION</a> structure that contains the changed application information.


## -remarks



"Application" is a set of software or software  features available on the peer's endpoint. Commonly, this refers to software packages that support peer networking activities, like games or other collaborative applications.

A peer's application has a GUID representing a single specific application. When an application is registered for a peer, this GUID and the corresponding application can be made available to all trusted contacts of the peer, indicating the activities the peer can participate in. To deregister a peer's application, call <a href="https://msdn.microsoft.com/2479b726-20f1-4370-9fcf-f29cec44c3ec">PeerCollabUnregisterApplication</a> with this GUID.

When a new application is registered locally using PeerCollabRegisterApplication or unregistered using PeerCollabUnregisterApplication all peers subscribed to the local peer's presence information receive the PEER_EVENT_ENDPOINT_APPLICATION_CHANGED event. Locally, applications receive the PEER_EVENT_MY_APPLICATION_CHANGED event. 

The <b>current user</b> scope has priority over the <b>all user</b> scope. If the application is registered in both scopes, the event will be fired only if the <b>current user</b> scope is changed.




## -see-also




<a href="https://msdn.microsoft.com/a219231b-75d0-47d3-8294-f1cc25b43d27">PEER_APPLICATION</a>



<a href="https://msdn.microsoft.com/ef8f1cc7-e1db-4d6d-9ff6-141746d0787a">PEER_CHANGE_TYPE</a>



<a href="https://msdn.microsoft.com/b84a17fc-35d6-4098-9bb3-18e708541a80">PEER_CONTACT</a>



<a href="https://msdn.microsoft.com/9687b332-14ed-4023-b8c2-437d75fd0298">PEER_ENDPOINT</a>



<a href="https://msdn.microsoft.com/2634899c-3263-45ce-9fac-407e11e42cd4">Peer Collaboration API Structures</a>
 

 

