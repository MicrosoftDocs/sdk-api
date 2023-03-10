---
UID: NS:p2p.peer_invitation_tag
title: PEER_INVITATION (p2p.h)
description: The PEER_INVITATION structure contains a request to initiate or join a peer collaboration activity.
helpviewer_keywords: ["*PPEER_INVITATION","PEER_INVITATION","PEER_INVITATION structure [Peer Networking]","PPEER_INVITATION","PPEER_INVITATION structure pointer [Peer Networking]","p2p.peer_invitation","p2p/PEER_INVITATION","p2p/PPEER_INVITATION"]
old-location: p2p\peer_invitation.htm
tech.root: p2p
ms.assetid: b74b45c0-760f-4008-87dd-9fdea0d4be05
ms.date: 12/05/2018
ms.keywords: '*PPEER_INVITATION, PEER_INVITATION, PEER_INVITATION structure [Peer Networking], PPEER_INVITATION, PPEER_INVITATION structure pointer [Peer Networking], p2p.peer_invitation, p2p/PEER_INVITATION, p2p/PPEER_INVITATION'
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
req.typenames: PEER_INVITATION, *PPEER_INVITATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_invitation_tag
 - p2p/peer_invitation_tag
 - PPEER_INVITATION
 - p2p/PPEER_INVITATION
 - PEER_INVITATION
 - p2p/PEER_INVITATION
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
 - PEER_INVITATION
---

# PEER_INVITATION structure


## -description

The <b>PEER_INVITATION</b> structure contains a request to initiate or join a peer collaboration activity.

## -struct-fields

### -field applicationId

GUID value that uniquely identifies the registered software or software component for the peer collaboration activity.

### -field applicationData

<a href="/windows/desktop/api/p2p/ns-p2p-peer_data">PEER_DATA</a> structure that contains opaque data describing possible additional application-specific settings (for example, an address and port on which the activity will occur, or a specific video codec to use). This data is limited to 16K.

### -field pwzMessage

Zero-terminated Unicode string that contains a specific request message to the invitation recipient. The message is limited to 255 unicode characters.

## -remarks

An invitation request is typically sent by a peer after a contact appears online within the peer collaboration network and a call to <a href="/windows/desktop/api/p2p/nf-p2p-peercollabenumapplications">PeerCollabEnumApplications</a> returns a common software application (represented as a application GUID) available on the contact's endpoint.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_data">PEER_DATA</a>



<a href="/windows/desktop/P2PSdk/collaboration-api-structures">Peer Collaboration API Structures</a>