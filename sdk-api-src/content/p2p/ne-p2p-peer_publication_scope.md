---
UID: NE:p2p.peer_publication_scope_tag
title: PEER_PUBLICATION_SCOPE (p2p.h)
description: Defines the set of scopes for the publication of peer objects or data.
helpviewer_keywords: ["PEER_PUBLICATION_SCOPE","PEER_PUBLICATION_SCOPE enumeration [Peer Networking]","PEER_PUBLICATION_SCOPE_ALL","PEER_PUBLICATION_SCOPE_INTERNET","PEER_PUBLICATION_SCOPE_NEAR_ME","PEER_PUBLICATION_SCOPE_NONE","p2p.peer_publication_scope","p2p/PEER_PUBLICATION_SCOPE","p2p/PEER_PUBLICATION_SCOPE_ALL","p2p/PEER_PUBLICATION_SCOPE_INTERNET","p2p/PEER_PUBLICATION_SCOPE_NEAR_ME","p2p/PEER_PUBLICATION_SCOPE_NONE"]
old-location: p2p\peer_publication_scope.htm
tech.root: p2p
ms.assetid: fecb9403-f790-4955-a879-fb3e6fbfe8ca
ms.date: 12/05/2018
ms.keywords: PEER_PUBLICATION_SCOPE, PEER_PUBLICATION_SCOPE enumeration [Peer Networking], PEER_PUBLICATION_SCOPE_ALL, PEER_PUBLICATION_SCOPE_INTERNET, PEER_PUBLICATION_SCOPE_NEAR_ME, PEER_PUBLICATION_SCOPE_NONE, p2p.peer_publication_scope, p2p/PEER_PUBLICATION_SCOPE, p2p/PEER_PUBLICATION_SCOPE_ALL, p2p/PEER_PUBLICATION_SCOPE_INTERNET, p2p/PEER_PUBLICATION_SCOPE_NEAR_ME, p2p/PEER_PUBLICATION_SCOPE_NONE
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
req.typenames: PEER_PUBLICATION_SCOPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_publication_scope_tag
 - p2p/peer_publication_scope_tag
 - PEER_PUBLICATION_SCOPE
 - p2p/PEER_PUBLICATION_SCOPE
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
 - PEER_PUBLICATION_SCOPE
---

# PEER_PUBLICATION_SCOPE enumeration


## -description

The <b>PEER_PUBLICATION_SCOPE</b> enumeration defines the set of scopes for the publication of peer objects or data.

## -enum-fields

### -field PEER_PUBLICATION_SCOPE_NONE:0x0

No scope is set for the publication of this data.

### -field PEER_PUBLICATION_SCOPE_NEAR_ME:0x1

The data is published to peers in the same logical or virtual subnet.

### -field PEER_PUBLICATION_SCOPE_INTERNET:0x2

The data is published to peers on the Internet.

### -field PEER_PUBLICATION_SCOPE_ALL

The data is published to all peers.

## -see-also

<a href="/windows/desktop/P2PSdk/collaboration-api-enumerations">Collaboration API Enumerations</a>
