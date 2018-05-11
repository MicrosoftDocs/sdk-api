---
UID: NS:p2p.peer_object_tag
title: peer_object_tag
author: windows-driver-content
description: The PEER_OBJECT structure contains application-specific run-time information that can be shared with trusted contacts within a peer collaboration network.
old-location: p2p\peer_object.htm
old-project: P2PSdk
ms.assetid: 6babceaf-9648-4226-a0ce-6f4ae831e4a7
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: "*PPEER_OBJECT, PCPEER_OBJECT, PCPEER_OBJECT structure pointer [Peer Networking], PEER_OBJECT, PEER_OBJECT structure [Peer Networking], PPEER_OBJECT, PPEER_OBJECT structure pointer [Peer Networking], p2p.peer_object, p2p/PCPEER_OBJECT, p2p/PEER_OBJECT, p2p/PPEER_OBJECT, peer_object_tag"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: PEER_OBJECT, *PPEER_OBJECT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	P2P.h
api_name:
-	PEER_OBJECT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# peer_object_tag structure


## -description


The <b>PEER_OBJECT</b> structure contains application-specific run-time information that can be shared with trusted contacts within a peer collaboration network.


## -struct-fields




### -field id

GUID value under which the peer object is uniquely registered.


### -field data


<a href="https://msdn.microsoft.com/d8a8b9e3-c455-4813-b812-263efe7f5e3e">PEER_DATA</a> structure that contains information which describes the peer object.


### -field dwPublicationScope


<a href="https://msdn.microsoft.com/fecb9403-f790-4955-a879-fb3e6fbfe8ca">PEER_PUBLICATION_SCOPE</a> enumeration value that specifies the publication scope for this peer object.


## -remarks



Peer objects are run-time data items associated with a particular application, such as a picture or avatar, a certificate, or a specific description. Each peer object must be smaller than 16K in size.

Trusted contacts watching this peer object will have a PEER_EVENT_OBJECT_CHANGED event raised on them signaling this peer object's change in status.

Peer object information is contained in the <b>data</b> member of this structure and  represented as a byte buffer with a maximum size of 16K.

The lifetime of a peer object is tied to the lifetime of the application that registered it.




## -see-also




<a href="https://msdn.microsoft.com/d8a8b9e3-c455-4813-b812-263efe7f5e3e">PEER_DATA</a>



<a href="https://msdn.microsoft.com/2634899c-3263-45ce-9fac-407e11e42cd4">Peer Collaboration API Structures</a>
 

 

