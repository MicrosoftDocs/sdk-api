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

# peer_graph_scope_tag enumeration


## -description


The <b>PEER_GRAPH_SCOPE</b> enumeration specifies the network scope of a peer graph.


## -enum-fields




### -field PEER_GRAPH_SCOPE_ANY

The peer graph's network scope can contain any IP address, valid or otherwise.


### -field PEER_GRAPH_SCOPE_GLOBAL

The IP addresses for the peer graph's network scope can be from any unblocked address range.


### -field PEER_GRAPH_SCOPE_SITELOCAL

The IP addresses for the peer graph's network scope must be within the IP range defined for the site.


### -field PEER_GRAPH_SCOPE_LINKLOCAL

The IP addresses for the peer graph's network scope must be within the IP range defined for the local area network.


### -field PEER_GRAPH_SCOPE_LOOPBACK

The peer graph's network scope is the local computer's loopback IP address.

