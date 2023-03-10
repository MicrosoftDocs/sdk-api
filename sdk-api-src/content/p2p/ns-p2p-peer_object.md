---
UID: NS:p2p.peer_object_tag
title: PEER_OBJECT (p2p.h)
description: The PEER_OBJECT structure contains application-specific run-time information that can be shared with trusted contacts within a peer collaboration network.
helpviewer_keywords: ["*PPEER_OBJECT","PCPEER_OBJECT","PCPEER_OBJECT structure pointer [Peer Networking]","PEER_OBJECT","PEER_OBJECT structure [Peer Networking]","PPEER_OBJECT","PPEER_OBJECT structure pointer [Peer Networking]","p2p.peer_object","p2p/PCPEER_OBJECT","p2p/PEER_OBJECT","p2p/PPEER_OBJECT"]
old-location: p2p\peer_object.htm
tech.root: p2p
ms.assetid: 6babceaf-9648-4226-a0ce-6f4ae831e4a7
ms.date: 12/05/2018
ms.keywords: '*PPEER_OBJECT, PCPEER_OBJECT, PCPEER_OBJECT structure pointer [Peer Networking], PEER_OBJECT, PEER_OBJECT structure [Peer Networking], PPEER_OBJECT, PPEER_OBJECT structure pointer [Peer Networking], p2p.peer_object, p2p/PCPEER_OBJECT, p2p/PEER_OBJECT, p2p/PPEER_OBJECT'
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
req.typenames: PEER_OBJECT, *PPEER_OBJECT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_object_tag
 - p2p/peer_object_tag
 - PPEER_OBJECT
 - p2p/PPEER_OBJECT
 - PEER_OBJECT
 - p2p/PEER_OBJECT
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
 - PEER_OBJECT
---

# PEER_OBJECT structure


## -description

The <b>PEER_OBJECT</b> structure contains application-specific run-time information that can be shared with trusted contacts within a peer collaboration network.

## -struct-fields

### -field id

GUID value under which the peer object is uniquely registered.

### -field data

<a href="/windows/desktop/api/p2p/ns-p2p-peer_data">PEER_DATA</a> structure that contains information which describes the peer object.

### -field dwPublicationScope

<a href="/windows/desktop/api/p2p/ne-p2p-peer_publication_scope">PEER_PUBLICATION_SCOPE</a> enumeration value that specifies the publication scope for this peer object.

## -remarks

Peer objects are run-time data items associated with a particular application, such as a picture or avatar, a certificate, or a specific description. Each peer object must be smaller than 16K in size.

Trusted contacts watching this peer object will have a PEER_EVENT_OBJECT_CHANGED event raised on them signaling this peer object's change in status.

Peer object information is contained in the <b>data</b> member of this structure and  represented as a byte buffer with a maximum size of 16K.

The lifetime of a peer object is tied to the lifetime of the application that registered it.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_data">PEER_DATA</a>



<a href="/windows/desktop/P2PSdk/collaboration-api-structures">Peer Collaboration API Structures</a>