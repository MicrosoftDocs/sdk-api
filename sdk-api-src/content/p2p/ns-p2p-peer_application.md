---
UID: NS:p2p.peer_application_tag
title: PEER_APPLICATION (p2p.h)
description: The PEER_APPLICATION structure contains data describing a locally installed software application or component that can be registered and shared with trusted contacts within a peer collaboration network.
helpviewer_keywords: ["*PPEER_APPLICATION","PCPEER_APPLICATION","PCPEER_APPLICATION structure pointer [Peer Networking]","PEER_APPLICATION","PEER_APPLICATION structure [Peer Networking]","PPEER_APPLICATION","PPEER_APPLICATION structure pointer [Peer Networking]","p2p.peer_application","p2p/PCPEER_APPLICATION","p2p/PEER_APPLICATION","p2p/PPEER_APPLICATION"]
old-location: p2p\peer_application.htm
tech.root: p2p
ms.assetid: a219231b-75d0-47d3-8294-f1cc25b43d27
ms.date: 12/05/2018
ms.keywords: '*PPEER_APPLICATION, PCPEER_APPLICATION, PCPEER_APPLICATION structure pointer [Peer Networking], PEER_APPLICATION, PEER_APPLICATION structure [Peer Networking], PPEER_APPLICATION, PPEER_APPLICATION structure pointer [Peer Networking], p2p.peer_application, p2p/PCPEER_APPLICATION, p2p/PEER_APPLICATION, p2p/PPEER_APPLICATION'
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
req.typenames: PEER_APPLICATION, *PPEER_APPLICATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_application_tag
 - p2p/peer_application_tag
 - PPEER_APPLICATION
 - p2p/PPEER_APPLICATION
 - PEER_APPLICATION
 - p2p/PEER_APPLICATION
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
 - PEER_APPLICATION
---

# PEER_APPLICATION structure


## -description

The <b>PEER_APPLICATION</b> structure contains data describing a locally installed software application or component  that can be registered and shared with trusted contacts within a peer collaboration network.

## -struct-fields

### -field id

The GUID value under which the application is registered with the local computer.

### -field data

<a href="/windows/desktop/api/p2p/ns-p2p-peer_data">PEER_DATA</a> structure that contains the application information in a member byte buffer. This information is available to anyone who can query for the local peer's member information. This data is limited to 16K.

### -field pwzDescription

Pointer to a zero-terminated Unicode string that contains an optional  description of the local application. This description is limited to 255 unicode characters.

## -remarks

An "application" is a set of software or software  features available on the peer's endpoint. Commonly, this refers to software packages that support peer networking activities, like games or other collaborative applications.

A peer application has a GUID representing a single specific application. When an application is registered for a peer, this GUID and the corresponding application can be made available to all trusted contacts of the peer, indicating the activities the peer can participate in. To deregister a peer application, call <a href="/windows/desktop/api/p2p/nf-p2p-peercollabunregisterapplication">PeerCollabUnregisterApplication</a> with this GUID.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_data">PEER_DATA</a>



<a href="/windows/desktop/P2PSdk/collaboration-api-structures">Peer Collaboration API Structures</a>