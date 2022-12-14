---
UID: NE:p2p.peer_presence_status_tag
title: PEER_PRESENCE_STATUS (p2p.h)
description: The PEER_PRESENCE_STATUS enumeration defines the set of possible presence status settings available to a peer that participates in a peer collaboration network.
helpviewer_keywords: ["PEER_PRESENCE_AWAY","PEER_PRESENCE_BE_RIGHT_BACK","PEER_PRESENCE_BUSY","PEER_PRESENCE_IDLE","PEER_PRESENCE_OFFLINE","PEER_PRESENCE_ONLINE","PEER_PRESENCE_ON_THE_PHONE","PEER_PRESENCE_OUT_TO_LUNCH","PEER_PRESENCE_STATUS","PEER_PRESENCE_STATUS enumeration [Peer Networking]","p2p.peer_presence_status","p2p/PEER_PRESENCE_AWAY","p2p/PEER_PRESENCE_BE_RIGHT_BACK","p2p/PEER_PRESENCE_BUSY","p2p/PEER_PRESENCE_IDLE","p2p/PEER_PRESENCE_OFFLINE","p2p/PEER_PRESENCE_ONLINE","p2p/PEER_PRESENCE_ON_THE_PHONE","p2p/PEER_PRESENCE_OUT_TO_LUNCH","p2p/PEER_PRESENCE_STATUS"]
old-location: p2p\peer_presence_status.htm
tech.root: p2p
ms.assetid: 0f7f6fa8-5da4-4f59-b9ea-0117ff8a3e28
ms.date: 12/05/2018
ms.keywords: PEER_PRESENCE_AWAY, PEER_PRESENCE_BE_RIGHT_BACK, PEER_PRESENCE_BUSY, PEER_PRESENCE_IDLE, PEER_PRESENCE_OFFLINE, PEER_PRESENCE_ONLINE, PEER_PRESENCE_ON_THE_PHONE, PEER_PRESENCE_OUT_TO_LUNCH, PEER_PRESENCE_STATUS, PEER_PRESENCE_STATUS enumeration [Peer Networking], p2p.peer_presence_status, p2p/PEER_PRESENCE_AWAY, p2p/PEER_PRESENCE_BE_RIGHT_BACK, p2p/PEER_PRESENCE_BUSY, p2p/PEER_PRESENCE_IDLE, p2p/PEER_PRESENCE_OFFLINE, p2p/PEER_PRESENCE_ONLINE, p2p/PEER_PRESENCE_ON_THE_PHONE, p2p/PEER_PRESENCE_OUT_TO_LUNCH, p2p/PEER_PRESENCE_STATUS
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
req.typenames: PEER_PRESENCE_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_presence_status_tag
 - p2p/peer_presence_status_tag
 - PEER_PRESENCE_STATUS
 - p2p/PEER_PRESENCE_STATUS
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
 - PEER_PRESENCE_STATUS
---

# PEER_PRESENCE_STATUS enumeration


## -description

The <b>PEER_PRESENCE_STATUS</b> enumeration defines the set of possible presence status settings available to a peer that participates in a peer collaboration network. These settings can be set by a peer collaboration network endpoint to indicate the peer's current level of participation to its watchers.

## -enum-fields

### -field PEER_PRESENCE_OFFLINE:0

The user is offline.

### -field PEER_PRESENCE_OUT_TO_LUNCH:1

The user is currently "out to lunch" and unable to respond.

### -field PEER_PRESENCE_AWAY:2

The user is away and unable to respond.

### -field PEER_PRESENCE_BE_RIGHT_BACK:3

The user has stepped away from the application and will participate soon.

### -field PEER_PRESENCE_IDLE:4

The user is idling.

### -field PEER_PRESENCE_BUSY:5

The user is busy and does not wish to be disturbed.

### -field PEER_PRESENCE_ON_THE_PHONE:6

The user is currently on the phone and does not wish to be disturbed.

### -field PEER_PRESENCE_ONLINE:7

The user is actively participating in the peer collaboration network.

## -see-also

<a href="/windows/desktop/P2PSdk/collaboration-api-enumerations">Collaboration API Enumerations</a>
