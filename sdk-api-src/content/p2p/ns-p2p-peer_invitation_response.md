---
UID: NS:p2p.peer_invitation_response_tag
title: PEER_INVITATION_RESPONSE (p2p.h)
description: The PEER_INVITATION_RESPONSE structure contains a response to an invitation to join a peer collaboration activity.
helpviewer_keywords: ["*PPEER_INVITATION_RESPONSE","PCPEER_INVITATION_RESPONSE","PCPEER_INVITATION_RESPONSE structure pointer [Peer Networking]","PEER_INVITATION_RESPONSE","PEER_INVITATION_RESPONSE structure [Peer Networking]","PPEER_INVITATION_RESPONSE","PPEER_INVITATION_RESPONSE structure pointer [Peer Networking]","p2p.peer_invitation_response","p2p/PCPEER_INVITATION_RESPONSE","p2p/PEER_INVITATION_RESPONSE","p2p/PPEER_INVITATION_RESPONSE"]
old-location: p2p\peer_invitation_response.htm
tech.root: p2p
ms.assetid: 9f77c471-ef05-442f-aeae-afe67319b0ff
ms.date: 12/05/2018
ms.keywords: '*PPEER_INVITATION_RESPONSE, PCPEER_INVITATION_RESPONSE, PCPEER_INVITATION_RESPONSE structure pointer [Peer Networking], PEER_INVITATION_RESPONSE, PEER_INVITATION_RESPONSE structure [Peer Networking], PPEER_INVITATION_RESPONSE, PPEER_INVITATION_RESPONSE structure pointer [Peer Networking], p2p.peer_invitation_response, p2p/PCPEER_INVITATION_RESPONSE, p2p/PEER_INVITATION_RESPONSE, p2p/PPEER_INVITATION_RESPONSE'
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
req.typenames: PEER_INVITATION_RESPONSE, *PPEER_INVITATION_RESPONSE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_invitation_response_tag
 - p2p/peer_invitation_response_tag
 - PPEER_INVITATION_RESPONSE
 - p2p/PPEER_INVITATION_RESPONSE
 - PEER_INVITATION_RESPONSE
 - p2p/PEER_INVITATION_RESPONSE
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
 - PEER_INVITATION_RESPONSE
---

# PEER_INVITATION_RESPONSE structure


## -description

The <b>PEER_INVITATION_RESPONSE</b> structure contains a response to an invitation to join a peer collaboration activity.

## -struct-fields

### -field action

[PEER_INVITATION_RESPONSE_TYPE](./ne-p2p-peer_invitation_response_type.md) enumeration value that specifies the action the peer takes in response to the invitation.

### -field pwzMessage

Reserved. This member must be set to <b>NULL</b>, and is set exclusively by the Peer Collaboration infrastructure.

### -field hrExtendedInfo

Any extended information that is part of the response. This can include an error code corresponding to the failure on the recipient of the invitation.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_invitation">PEER_INVITATION</a>



<a href="/windows/desktop/P2PSdk/collaboration-api-structures">Peer Collaboration API Structures</a>