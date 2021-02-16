---
UID: NS:p2p.peer_people_near_me_tag
title: PEER_PEOPLE_NEAR_ME (p2p.h)
description: Contains information about a peer in the same logical or virtual subnet.
helpviewer_keywords: ["*PPEER_PEOPLE_NEAR_ME","PCPEER_PEOPLE_NEAR_ME","PCPEER_PEOPLE_NEAR_ME structure pointer [Peer Networking]","PEER_PEOPLE_NEAR_ME","PEER_PEOPLE_NEAR_ME structure [Peer Networking]","PPEER_PEOPLE_NEAR_ME","PPEER_PEOPLE_NEAR_ME structure pointer [Peer Networking]","PPPEER_PEOPLE_NEAR_ME","PPPEER_PEOPLE_NEAR_ME structure pointer [Peer Networking]","p2p.peer_people_near_me","p2p/PCPEER_PEOPLE_NEAR_ME","p2p/PEER_PEOPLE_NEAR_ME","p2p/PPEER_PEOPLE_NEAR_ME","p2p/PPPEER_PEOPLE_NEAR_ME"]
old-location: p2p\peer_people_near_me.htm
tech.root: p2p
ms.assetid: 15dae06d-0f44-4e7d-b146-6fcd7cc6912e
ms.date: 12/05/2018
ms.keywords: '*PPEER_PEOPLE_NEAR_ME, PCPEER_PEOPLE_NEAR_ME, PCPEER_PEOPLE_NEAR_ME structure pointer [Peer Networking], PEER_PEOPLE_NEAR_ME, PEER_PEOPLE_NEAR_ME structure [Peer Networking], PPEER_PEOPLE_NEAR_ME, PPEER_PEOPLE_NEAR_ME structure pointer [Peer Networking], PPPEER_PEOPLE_NEAR_ME, PPPEER_PEOPLE_NEAR_ME structure pointer [Peer Networking], p2p.peer_people_near_me, p2p/PCPEER_PEOPLE_NEAR_ME, p2p/PEER_PEOPLE_NEAR_ME, p2p/PPEER_PEOPLE_NEAR_ME, p2p/PPPEER_PEOPLE_NEAR_ME'
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
req.typenames: PEER_PEOPLE_NEAR_ME, *PPEER_PEOPLE_NEAR_ME
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_people_near_me_tag
 - p2p/peer_people_near_me_tag
 - PPEER_PEOPLE_NEAR_ME
 - p2p/PPEER_PEOPLE_NEAR_ME
 - PEER_PEOPLE_NEAR_ME
 - p2p/PEER_PEOPLE_NEAR_ME
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
 - PEER_PEOPLE_NEAR_ME
---

# PEER_PEOPLE_NEAR_ME structure


## -description

The <b>PEER_PEOPLE_NEAR_ME</b> structure contains information about a peer in the same logical or virtual subnet.

## -struct-fields

### -field pwzNickName

Zero-terminated Unicode string that contains the nickname of the contact.

### -field endpoint

<a href="/windows/desktop/api/p2p/ns-p2p-peer_endpoint">PEER_ENDPOINT</a> structure that contains the IPv6 network address of the peer whose endpoint shares the same subnet.

### -field id

GUID value that contains the unique ID value for this peer.  Since this value uniquely identifies a peer endpoint, the display name and even the associated IPv6 address can be changed with deleting the rest of the peer information.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_data">PEER_DATA</a>



<a href="/windows/desktop/P2PSdk/collaboration-api-structures">Peer Collaboration API Structures</a>