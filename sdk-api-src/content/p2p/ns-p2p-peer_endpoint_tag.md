---
UID: NS:p2p.peer_endpoint_tag
title: peer_endpoint_tag
author: windows-sdk-content
description: The PEER_ENDPOINT structure contains the address and friendly name of a peer endpoint.
old-location: p2p\peer_endpoint.htm
old-project: P2PSdk
ms.assetid: 9687b332-14ed-4023-b8c2-437d75fd0298
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: "*PPEER_ENDPOINT, PCPEER_ENDPOINT, PCPEER_ENDPOINT structure pointer [Peer Networking], PEER_ENDPOINT, PEER_ENDPOINT structure [Peer Networking], PPEER_ENDPOINT, PPEER_ENDPOINT structure pointer [Peer Networking], p2p.peer_endpoint, p2p/PCPEER_ENDPOINT, p2p/PEER_ENDPOINT, p2p/PPEER_ENDPOINT, peer_endpoint_tag"
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
tech.root: 
req.typenames: PEER_ENDPOINT, *PPEER_ENDPOINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	P2P.h
api_name:
-	PEER_ENDPOINT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# peer_endpoint_tag structure


## -description


The <b>PEER_ENDPOINT</b> structure contains the address and friendly name of a peer endpoint.


## -struct-fields




### -field address


<a href="https://msdn.microsoft.com/09476d3b-ec65-40a2-90ee-a20be230deca">PEER_ADDRESS</a> structure that contains the IPv6 network address of the endpoint.


### -field pwzEndpointName

Zero-terminated Unicode string that contains the specific displayable name of the endpoint.


## -remarks



A peer "endpoint" describes a contact's presence location — the unique network address configuration that describes the currently available instance of the contact within the peer collaboration network. A single contact can be available at multiple endpoints within the peer collaboration network.

A peer watching a contact can query any of the endpoints associated with that contact for specific peer presence, application, or object updates.




## -see-also




<a href="https://msdn.microsoft.com/09476d3b-ec65-40a2-90ee-a20be230deca">PEER_ADDRESS</a>



<a href="https://msdn.microsoft.com/2634899c-3263-45ce-9fac-407e11e42cd4">Peer Collaboration API Structures</a>
 

 

