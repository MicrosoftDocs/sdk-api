---
UID: NE:p2p.peer_signin_flags_tag
title: peer_signin_flags_tag
author: windows-sdk-content
description: The PEER_SIGNIN_FLAGS enumeration defines the set of peer presence publication behaviors available when the peer signs in to a peer collaboration network.
old-location: p2p\peer_signin_flags.htm
old-project: P2PSdk
ms.assetid: 00b7f57a-222d-4152-bded-93f1899692da
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: PEER_SIGNIN_ALL, PEER_SIGNIN_FLAGS, PEER_SIGNIN_FLAGS enumeration [Peer Networking], PEER_SIGNIN_INTERNET, PEER_SIGNIN_NEAR_ME, PEER_SIGNIN_NONE, p2p.peer_signin_flags, p2p/PEER_SIGNIN_ALL, p2p/PEER_SIGNIN_FLAGS, p2p/PEER_SIGNIN_INTERNET, p2p/PEER_SIGNIN_NEAR_ME, p2p/PEER_SIGNIN_NONE, peer_signin_flags_tag
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: PEER_SIGNIN_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	P2P.h
api_name:
-	PEER_SIGNIN_FLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# peer_signin_flags_tag enumeration


## -description


The <b>PEER_SIGNIN_FLAGS</b> enumeration defines the set of peer presence publication behaviors available when the peer signs in to a peer collaboration network.


## -enum-fields




### -field PEER_SIGNIN_NONE

A peer's presence is not being published in any scope.


### -field PEER_SIGNIN_NEAR_ME

The peer can publish availability information to endpoints in the same subnet or local area network, or query for other endpoints available on the subnet.


### -field PEER_SIGNIN_INTERNET

The peer can publish presence, applications, and objects to all contacts in a peer's contact list.



### -field PEER_SIGNIN_ALL

The peer can publish presence, applications, and objects to all contacts in a peer's contact list, or query for other endpoints available on the subnet.


## -see-also




<a href="https://msdn.microsoft.com/f72e372a-0d23-47f4-8518-1296ec81ce55">Collaboration API Enumerations</a>
 

 

