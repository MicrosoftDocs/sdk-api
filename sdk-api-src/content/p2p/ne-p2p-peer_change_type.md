---
UID: NE:p2p.peer_change_type_tag
title: PEER_CHANGE_TYPE (p2p.h)
description: The PEER_CHANGE_TYPE enumeration defines the set of changes that were performed on a peer object, endpoint, or application in a peer event. It is used to qualify the peer event associated with the change type.
helpviewer_keywords: ["PEER_CHANGE_ADDED","PEER_CHANGE_DELETED","PEER_CHANGE_TYPE","PEER_CHANGE_TYPE enumeration [Peer Networking]","PEER_CHANGE_UPDATED","p2p.peer_change_type","p2p/PEER_CHANGE_ADDED","p2p/PEER_CHANGE_DELETED","p2p/PEER_CHANGE_TYPE","p2p/PEER_CHANGE_UPDATED"]
old-location: p2p\peer_change_type.htm
tech.root: p2p
ms.assetid: ef8f1cc7-e1db-4d6d-9ff6-141746d0787a
ms.date: 12/05/2018
ms.keywords: PEER_CHANGE_ADDED, PEER_CHANGE_DELETED, PEER_CHANGE_TYPE, PEER_CHANGE_TYPE enumeration [Peer Networking], PEER_CHANGE_UPDATED, p2p.peer_change_type, p2p/PEER_CHANGE_ADDED, p2p/PEER_CHANGE_DELETED, p2p/PEER_CHANGE_TYPE, p2p/PEER_CHANGE_UPDATED
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
req.typenames: PEER_CHANGE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_change_type_tag
 - p2p/peer_change_type_tag
 - PEER_CHANGE_TYPE
 - p2p/PEER_CHANGE_TYPE
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
 - PEER_CHANGE_TYPE
---

# PEER_CHANGE_TYPE enumeration


## -description

The <b>PEER_CHANGE_TYPE</b> enumeration defines the set of changes that were performed on a peer object, endpoint, or application in a peer event. It is used to qualify the peer event associated with the change type.

## -enum-fields

### -field PEER_CHANGE_ADDED:0

The peer object, endpoint, or application has been added.

### -field PEER_CHANGE_DELETED:1

The peer object, endpoint, or application has been deleted.

### -field PEER_CHANGE_UPDATED:2

The peer object, endpoint, or application has been updated with new information.

## -see-also

<a href="/windows/desktop/P2PSdk/collaboration-api-enumerations">Collaboration API Enumerations</a>
