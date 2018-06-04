---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# peer_collab_event_type_tag enumeration


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
 

 

