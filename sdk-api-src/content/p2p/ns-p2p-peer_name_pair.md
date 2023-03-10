---
UID: NS:p2p.peer_name_pair_tag
title: PEER_NAME_PAIR (p2p.h)
description: The PEER_NAME_PAIR structure contains the results of a call to PeerGetNextItem.
helpviewer_keywords: ["*PPEER_NAME_PAIR","PEER_NAME_PAIR","PEER_NAME_PAIR structure [Peer Networking]","PPEER_NAME_PAIR","PPEER_NAME_PAIR structure pointer [Peer Networking]","p2p.peer_name_pair","p2p/PPEER_NAME_PAIR","p2p/peer_name_pair_tag"]
old-location: p2p\peer_name_pair.htm
tech.root: p2p
ms.assetid: 4c64664e-33c6-490e-b160-7bdb5fb428fa
ms.date: 12/05/2018
ms.keywords: '*PPEER_NAME_PAIR, PEER_NAME_PAIR, PEER_NAME_PAIR structure [Peer Networking], PPEER_NAME_PAIR, PPEER_NAME_PAIR structure pointer [Peer Networking], p2p.peer_name_pair, p2p/PPEER_NAME_PAIR, p2p/peer_name_pair_tag'
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only],Windows XP with SP1 with the Advanced Networking Pack for Windows XP
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
req.typenames: PEER_NAME_PAIR, *PPEER_NAME_PAIR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_name_pair_tag
 - p2p/peer_name_pair_tag
 - PPEER_NAME_PAIR
 - p2p/PPEER_NAME_PAIR
 - PEER_NAME_PAIR
 - p2p/PEER_NAME_PAIR
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
 - PEER_NAME_PAIR
---

# PEER_NAME_PAIR structure


## -description

The <b>PEER_NAME_PAIR</b> structure contains the results of a call to  <a href="/windows/desktop/api/p2p/nf-p2p-peergetnextitem">PeerGetNextItem</a>.

## -struct-fields

### -field dwSize

Specifies the size, in bytes, of this structure.

### -field pwzPeerName

Specifies the peer name of the peer identity or peer group.

### -field pwzFriendlyName

Specifies the friendly name of the peer identity or peer group.

## -remarks

This structure is used when enumerating peer identities and peer groups associated with a specific identity.

When enumerating peer identities, each <b>PEER_NAME_PAIR</b> structure contains a peer name and the friendly name of the identity.

When enumerating peer groups,  each <b>PEER_NAME_PAIR</b>  structure contains the peer name and friendly name of the corresponding peer group.

## -see-also

<a href="/windows/desktop/api/p2p/nf-p2p-peerenumgroups">PeerEnumGroups</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peerenumidentities">PeerEnumIdentities</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergetnextitem">PeerGetNextItem</a>