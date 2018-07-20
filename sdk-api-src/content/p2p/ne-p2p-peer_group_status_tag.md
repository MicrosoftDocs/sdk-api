---
UID: NE:p2p.peer_group_status_tag
title: peer_group_status_tag
author: windows-sdk-content
description: The PEER_GROUP_STATUS flags indicate whether or not the peer group has connections present.
old-location: p2p\peer_group_status.htm
old-project: p2psdk
ms.assetid: ed3fa9a6-5180-419f-b5d1-02889bbcdd0d
ms.author: windowssdkdev
ms.date: 07/17/2018
ms.keywords: PEER_GROUP_STATUS, PEER_GROUP_STATUS enumeration [Peer Networking], PEER_GROUP_STATUS_HAS_CONNECTIONS, PEER_GROUP_STATUS_LISTENING, p2p.peer_group_status, p2p/ PEER_GROUP_STATUS, p2p/PEER_GROUP_STATUS_HAS_CONNECTIONS, p2p/PEER_GROUP_STATUS_LISTENING, peer_group_status_tag
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only],Windows XP with SP1with the Advanced Networking Pack forWindows XP
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
req.typenames: PEER_GROUP_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - P2P.h
api_name:
 - PEER_GROUP_STATUS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# peer_group_status_tag enumeration


## -description



      The <b>PEER_GROUP_STATUS</b> flags indicate whether or not the peer group has connections present.


## -enum-fields




### -field PEER_GROUP_STATUS_LISTENING

The peer group is awaiting new connections.


### -field PEER_GROUP_STATUS_HAS_CONNECTIONS

The peer group has at least one connection.


## -see-also




<a href="https://msdn.microsoft.com/5cdae832-e6a7-481c-9784-1c1c07d689dd">
        PEER_GROUP_EVENT_DATA</a>



<a href="https://msdn.microsoft.com/712e6473-bb49-460a-9761-69a5ee4a067e">PeerGroupGetStatus</a>
 

 

