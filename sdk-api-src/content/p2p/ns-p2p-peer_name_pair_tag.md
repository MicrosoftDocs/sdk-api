---
UID: NS:p2p.peer_name_pair_tag
title: peer_name_pair_tag
author: windows-sdk-content
description: The PEER_NAME_PAIR structure contains the results of a call to PeerGetNextItem.
old-location: p2p\peer_name_pair.htm
old-project: P2PSdk
ms.assetid: 4c64664e-33c6-490e-b160-7bdb5fb428fa
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: "*PPEER_NAME_PAIR, PEER_NAME_PAIR, PEER_NAME_PAIR structure [Peer Networking], PPEER_NAME_PAIR, PPEER_NAME_PAIR structure pointer [Peer Networking], p2p.peer_name_pair, p2p/PPEER_NAME_PAIR, p2p/peer_name_pair_tag, peer_name_pair_tag"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: PEER_NAME_PAIR, *PPEER_NAME_PAIR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - P2P.h
api_name:
 - PEER_NAME_PAIR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# peer_name_pair_tag structure


## -description


The <b>PEER_NAME_PAIR</b> structure contains the results of a call to  <a href="https://msdn.microsoft.com/015faeb3-82d9-49e5-a451-7394bf83240f">PeerGetNextItem</a>.


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




<a href="https://msdn.microsoft.com/debb3c57-b5d2-440b-acf2-b6d8e712849b">PeerEnumGroups</a>



<a href="https://msdn.microsoft.com/91f18185-0292-41a3-8aff-8b345cab5e82">PeerEnumIdentities</a>



<a href="https://msdn.microsoft.com/015faeb3-82d9-49e5-a451-7394bf83240f">PeerGetNextItem</a>
 

 

