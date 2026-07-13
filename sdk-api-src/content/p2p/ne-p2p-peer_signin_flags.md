---
UID: NE:p2p.peer_signin_flags_tag
title: PEER_SIGNIN_FLAGS (p2p.h)
description: The PEER_SIGNIN_FLAGS enumeration defines the set of peer presence publication behaviors available when the peer signs in to a peer collaboration network.
helpviewer_keywords: ["PEER_SIGNIN_ALL","PEER_SIGNIN_FLAGS","PEER_SIGNIN_FLAGS enumeration [Peer Networking]","PEER_SIGNIN_INTERNET","PEER_SIGNIN_NEAR_ME","PEER_SIGNIN_NONE","p2p.peer_signin_flags","p2p/PEER_SIGNIN_ALL","p2p/PEER_SIGNIN_FLAGS","p2p/PEER_SIGNIN_INTERNET","p2p/PEER_SIGNIN_NEAR_ME","p2p/PEER_SIGNIN_NONE"]
old-location: p2p\peer_signin_flags.htm
tech.root: p2p
ms.assetid: 00b7f57a-222d-4152-bded-93f1899692da
ms.date: 12/05/2018
ms.keywords: PEER_SIGNIN_ALL, PEER_SIGNIN_FLAGS, PEER_SIGNIN_FLAGS enumeration [Peer Networking], PEER_SIGNIN_INTERNET, PEER_SIGNIN_NEAR_ME, PEER_SIGNIN_NONE, p2p.peer_signin_flags, p2p/PEER_SIGNIN_ALL, p2p/PEER_SIGNIN_FLAGS, p2p/PEER_SIGNIN_INTERNET, p2p/PEER_SIGNIN_NEAR_ME, p2p/PEER_SIGNIN_NONE
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
req.typenames: PEER_SIGNIN_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_signin_flags_tag
 - p2p/peer_signin_flags_tag
 - PEER_SIGNIN_FLAGS
 - p2p/PEER_SIGNIN_FLAGS
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
 - PEER_SIGNIN_FLAGS
---

# PEER_SIGNIN_FLAGS enumeration


## -description

The <b>PEER_SIGNIN_FLAGS</b> enumeration defines the set of peer presence publication behaviors available when the peer signs in to a peer collaboration network.

## -enum-fields

### -field PEER_SIGNIN_NONE:0x0

A peer's presence is not being published in any scope.

### -field PEER_SIGNIN_NEAR_ME:0x1

The peer can publish availability information to endpoints in the same subnet or local area network, or query for other endpoints available on the subnet.

### -field PEER_SIGNIN_INTERNET:0x2

The peer can publish presence, applications, and objects to all contacts in a peer's contact list.

### -field PEER_SIGNIN_ALL

The peer can publish presence, applications, and objects to all contacts in a peer's contact list, or query for other endpoints available on the subnet.

## -see-also

<a href="/windows/desktop/P2PSdk/collaboration-api-enumerations">Collaboration API Enumerations</a>
