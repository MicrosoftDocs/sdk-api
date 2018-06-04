---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

