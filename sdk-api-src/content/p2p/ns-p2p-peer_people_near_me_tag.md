---
UID: NS:p2p.peer_people_near_me_tag
title: peer_people_near_me_tag
author: windows-sdk-content
description: Contains information about a peer in the same logical or virtual subnet.
old-location: p2p\peer_people_near_me.htm
old-project: P2PSdk
ms.assetid: 15dae06d-0f44-4e7d-b146-6fcd7cc6912e
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: "*PPEER_PEOPLE_NEAR_ME, PCPEER_PEOPLE_NEAR_ME, PCPEER_PEOPLE_NEAR_ME structure pointer [Peer Networking], PEER_PEOPLE_NEAR_ME, PEER_PEOPLE_NEAR_ME structure [Peer Networking], PPEER_PEOPLE_NEAR_ME, PPEER_PEOPLE_NEAR_ME structure pointer [Peer Networking], PPPEER_PEOPLE_NEAR_ME, PPPEER_PEOPLE_NEAR_ME structure pointer [Peer Networking], p2p.peer_people_near_me, p2p/PCPEER_PEOPLE_NEAR_ME, p2p/PEER_PEOPLE_NEAR_ME, p2p/PPEER_PEOPLE_NEAR_ME, p2p/PPPEER_PEOPLE_NEAR_ME, peer_people_near_me_tag"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: PEER_PEOPLE_NEAR_ME, *PPEER_PEOPLE_NEAR_ME
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - P2P.h
api_name:
 - PEER_PEOPLE_NEAR_ME
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# peer_people_near_me_tag structure


## -description


The <b>PEER_PEOPLE_NEAR_ME</b> structure contains information about a peer in the same logical or virtual subnet.


## -struct-fields




### -field pwzNickName

Zero-terminated Unicode string that contains the nickname of the contact.


### -field endpoint


<a href="https://msdn.microsoft.com/9687b332-14ed-4023-b8c2-437d75fd0298">PEER_ENDPOINT</a> structure that contains the IPv6 network address of the peer whose endpoint shares the same subnet.


### -field id

GUID value that contains the unique ID value for this peer.  Since this value uniquely identifies a peer endpoint, the display name and even the associated IPv6 address can be changed with deleting the rest of the peer information.


## -see-also




<a href="https://msdn.microsoft.com/d8a8b9e3-c455-4813-b812-263efe7f5e3e">PEER_DATA</a>



<a href="https://msdn.microsoft.com/2634899c-3263-45ce-9fac-407e11e42cd4">Peer Collaboration API Structures</a>
 

 

