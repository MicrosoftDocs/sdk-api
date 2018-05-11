---
UID: NE:p2p.peer_group_authentication_scheme_tag
title: peer_group_authentication_scheme_tag
author: windows-driver-content
description: Defines the set of possible authentication schemes that can be used to authenticate peers joining a peer group.
old-location: p2p\peer_group_authentication_scheme.htm
old-project: P2PSdk
ms.assetid: 51bbbfdb-fa64-473b-aa48-2562512a2af3
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: PEER_GROUP_AUTHENTICATION_SCHEME, PEER_GROUP_AUTHENTICATION_SCHEME enumeration [Peer Networking], PEER_GROUP_GMC_AUTHENTICATION, PEER_GROUP_PASSWORD_AUTHENTICATION, p2p.peer_group_authentication_scheme, p2p/PEER_GROUP_AUTHENTICATION_SCHEME, p2p/PEER_GROUP_GMC_AUTHENTICATION, p2p/PEER_GROUP_PASSWORD_AUTHENTICATION, peer_group_authentication_scheme_tag
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: PEER_GROUP_AUTHENTICATION_SCHEME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	P2P.h
api_name:
-	PEER_GROUP_AUTHENTICATION_SCHEME
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# peer_group_authentication_scheme_tag enumeration


## -description


The <b>PEER_GROUP_AUTHENTICATION_SCHEME</b> enumeration defines the set of possible authentication schemes that can be used to authenticate peers joining a peer group.


## -enum-fields




### -field PEER_GROUP_GMC_AUTHENTICATION

Authentication is performed using Group Membership Certificates (GMC).


### -field PEER_GROUP_PASSWORD_AUTHENTICATION

Authentication is performed by validating a provided password.

