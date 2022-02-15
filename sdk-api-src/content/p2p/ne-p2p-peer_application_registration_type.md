---
UID: NE:p2p.peer_application_registration_type_tag
title: PEER_APPLICATION_REGISTRATION_TYPE (p2p.h)
description: The PEER_APPLICATION_REGISTRATION_TYPE enumeration defines the set of peer application registration flags.
helpviewer_keywords: ["PEER_APPLICATION_ALL_USERS","PEER_APPLICATION_CURRENT_USER","PEER_APPLICATION_REGISTRATION_TYPE","PEER_APPLICATION_REGISTRATION_TYPE enumeration [Peer Networking]","p2p.peer_application_registration_type","p2p/PEER_APPLICATION_ALL_USERS","p2p/PEER_APPLICATION_CURRENT_USER","p2p/PEER_APPLICATION_REGISTRATION_TYPE"]
old-location: p2p\peer_application_registration_type.htm
tech.root: p2p
ms.assetid: 58f14e46-377e-494b-93ef-fc19e8d87fcc
ms.date: 12/05/2018
ms.keywords: PEER_APPLICATION_ALL_USERS, PEER_APPLICATION_CURRENT_USER, PEER_APPLICATION_REGISTRATION_TYPE, PEER_APPLICATION_REGISTRATION_TYPE enumeration [Peer Networking], p2p.peer_application_registration_type, p2p/PEER_APPLICATION_ALL_USERS, p2p/PEER_APPLICATION_CURRENT_USER, p2p/PEER_APPLICATION_REGISTRATION_TYPE
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
req.typenames: PEER_APPLICATION_REGISTRATION_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_application_registration_type_tag
 - p2p/peer_application_registration_type_tag
 - PEER_APPLICATION_REGISTRATION_TYPE
 - p2p/PEER_APPLICATION_REGISTRATION_TYPE
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
 - PEER_APPLICATION_REGISTRATION_TYPE
---

# PEER_APPLICATION_REGISTRATION_TYPE enumeration


## -description

The <b>PEER_APPLICATION_REGISTRATION_TYPE</b> enumeration defines the set of peer application registration flags.

## -enum-fields

### -field PEER_APPLICATION_CURRENT_USER:0

The application is available only to the current user account logged into the machine.

### -field PEER_APPLICATION_ALL_USERS:1

The application is available to all user accounts set on the machine.

## -remarks

"Peer application" defines the set of software applications or components available for use with the peer collaboration network. The peer collaboration network enables participants in the network to initiate usage of this application.

Applications with the same GUID and registered for the <b>current user</b>  take precedence over applications with that same GUID registered for <b>all users</b>.

## -see-also

<a href="/windows/desktop/P2PSdk/collaboration-api-enumerations">Collaboration API Enumerations</a>
