---
UID: NE:p2p.peer_group_authentication_scheme_tag
title: PEER_GROUP_AUTHENTICATION_SCHEME (p2p.h)
description: Defines the set of possible authentication schemes that can be used to authenticate peers joining a peer group.
helpviewer_keywords: ["PEER_GROUP_AUTHENTICATION_SCHEME","PEER_GROUP_AUTHENTICATION_SCHEME enumeration [Peer Networking]","PEER_GROUP_GMC_AUTHENTICATION","PEER_GROUP_PASSWORD_AUTHENTICATION","p2p.peer_group_authentication_scheme","p2p/PEER_GROUP_AUTHENTICATION_SCHEME","p2p/PEER_GROUP_GMC_AUTHENTICATION","p2p/PEER_GROUP_PASSWORD_AUTHENTICATION"]
old-location: p2p\peer_group_authentication_scheme.htm
tech.root: p2p
ms.assetid: 51bbbfdb-fa64-473b-aa48-2562512a2af3
ms.date: 12/05/2018
ms.keywords: PEER_GROUP_AUTHENTICATION_SCHEME, PEER_GROUP_AUTHENTICATION_SCHEME enumeration [Peer Networking], PEER_GROUP_GMC_AUTHENTICATION, PEER_GROUP_PASSWORD_AUTHENTICATION, p2p.peer_group_authentication_scheme, p2p/PEER_GROUP_AUTHENTICATION_SCHEME, p2p/PEER_GROUP_GMC_AUTHENTICATION, p2p/PEER_GROUP_PASSWORD_AUTHENTICATION
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
req.typenames: PEER_GROUP_AUTHENTICATION_SCHEME
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_group_authentication_scheme_tag
 - p2p/peer_group_authentication_scheme_tag
 - PEER_GROUP_AUTHENTICATION_SCHEME
 - p2p/PEER_GROUP_AUTHENTICATION_SCHEME
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
 - PEER_GROUP_AUTHENTICATION_SCHEME
---

# PEER_GROUP_AUTHENTICATION_SCHEME enumeration


## -description

The <b>PEER_GROUP_AUTHENTICATION_SCHEME</b> enumeration defines the set of possible authentication schemes that can be used to authenticate peers joining a peer group.

## -enum-fields

### -field PEER_GROUP_GMC_AUTHENTICATION:0x00000001

Authentication is performed using Group Membership Certificates (GMC).

### -field PEER_GROUP_PASSWORD_AUTHENTICATION:0x00000002

Authentication is performed by validating a provided password.

