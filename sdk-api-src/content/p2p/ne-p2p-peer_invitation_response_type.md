---
UID: NE:p2p.peer_invitation_response_type_tag
title: PEER_INVITATION_RESPONSE_TYPE (p2p.h)
description: Defines the type of response received to an invitation to start a Peer Collaboration activity.
helpviewer_keywords: ["PEER_INVITATION_RESPONSE_ACCEPTED","PEER_INVITATION_RESPONSE_DECLINED","PEER_INVITATION_RESPONSE_ERROR","PEER_INVITATION_RESPONSE_EXPIRED","PEER_INVITATION_RESPONSE_TYPE","PEER_INVITATION_RESPONSE_TYPE enumeration [Peer Networking]","p2p.peer_invitation_response_type","p2p/PEER_INVITATION_RESPONSE_ACCEPTED","p2p/PEER_INVITATION_RESPONSE_DECLINED","p2p/PEER_INVITATION_RESPONSE_ERROR","p2p/PEER_INVITATION_RESPONSE_EXPIRED","p2p/PEER_INVITATION_RESPONSE_TYPE"]
old-location: p2p\peer_invitation_response_type.htm
tech.root: p2p
ms.assetid: ad456eb5-a28c-4826-976f-e38e2f269ff0
ms.date: 12/05/2018
ms.keywords: PEER_INVITATION_RESPONSE_ACCEPTED, PEER_INVITATION_RESPONSE_DECLINED, PEER_INVITATION_RESPONSE_ERROR, PEER_INVITATION_RESPONSE_EXPIRED, PEER_INVITATION_RESPONSE_TYPE, PEER_INVITATION_RESPONSE_TYPE enumeration [Peer Networking], p2p.peer_invitation_response_type, p2p/PEER_INVITATION_RESPONSE_ACCEPTED, p2p/PEER_INVITATION_RESPONSE_DECLINED, p2p/PEER_INVITATION_RESPONSE_ERROR, p2p/PEER_INVITATION_RESPONSE_EXPIRED, p2p/PEER_INVITATION_RESPONSE_TYPE
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
req.typenames: PEER_INVITATION_RESPONSE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_invitation_response_type_tag
 - p2p/peer_invitation_response_type_tag
 - PEER_INVITATION_RESPONSE_TYPE
 - p2p/PEER_INVITATION_RESPONSE_TYPE
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
 - PEER_INVITATION_RESPONSE_TYPE
---

# PEER_INVITATION_RESPONSE_TYPE enumeration


## -description

The <b>PEER_INVITATION_RESPONSE_TYPE</b> enumeration defines the type of  response received to an invitation to start a Peer Collaboration activity.

## -enum-fields

### -field PEER_INVITATION_RESPONSE_DECLINED:0

The invitation was declined by the peer.

### -field PEER_INVITATION_RESPONSE_ACCEPTED:1

The invitation was accepted by the peer.

### -field PEER_INVITATION_RESPONSE_EXPIRED:2

The invitation has expired.

### -field PEER_INVITATION_RESPONSE_ERROR:3

An error occurred during the invitation process.

## -see-also

<a href="/windows/desktop/P2PSdk/collaboration-api-enumerations">Collaboration API Enumerations</a>
