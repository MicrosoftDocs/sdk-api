---
UID: NE:p2p.peer_graph_scope_tag
title: PEER_GRAPH_SCOPE (p2p.h)
description: The PEER_GRAPH_SCOPE enumeration specifies the network scope of a peer graph.
helpviewer_keywords: ["PEER_GRAPH_SCOPE","PEER_GRAPH_SCOPE enumeration [Peer Networking]","PEER_GRAPH_SCOPE_ANY","PEER_GRAPH_SCOPE_GLOBAL","PEER_GRAPH_SCOPE_LINKLOCAL","PEER_GRAPH_SCOPE_LOOPBACK","PEER_GRAPH_SCOPE_SITELOCAL","p2p.peer_graph_scope","p2p/PEER_GRAPH_SCOPE","p2p/PEER_GRAPH_SCOPE_ANY","p2p/PEER_GRAPH_SCOPE_GLOBAL","p2p/PEER_GRAPH_SCOPE_LINKLOCAL","p2p/PEER_GRAPH_SCOPE_LOOPBACK","p2p/PEER_GRAPH_SCOPE_SITELOCAL"]
old-location: p2p\peer_graph_scope.htm
tech.root: p2p
ms.assetid: 103f0493-05b9-46a6-8304-0c38ec7dc674
ms.date: 12/05/2018
ms.keywords: PEER_GRAPH_SCOPE, PEER_GRAPH_SCOPE enumeration [Peer Networking], PEER_GRAPH_SCOPE_ANY, PEER_GRAPH_SCOPE_GLOBAL, PEER_GRAPH_SCOPE_LINKLOCAL, PEER_GRAPH_SCOPE_LOOPBACK, PEER_GRAPH_SCOPE_SITELOCAL, p2p.peer_graph_scope, p2p/PEER_GRAPH_SCOPE, p2p/PEER_GRAPH_SCOPE_ANY, p2p/PEER_GRAPH_SCOPE_GLOBAL, p2p/PEER_GRAPH_SCOPE_LINKLOCAL, p2p/PEER_GRAPH_SCOPE_LOOPBACK, p2p/PEER_GRAPH_SCOPE_SITELOCAL
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only],Windows XP with SP1 with the Advanced Networking Pack forWindows XP
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
req.typenames: PEER_GRAPH_SCOPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_graph_scope_tag
 - p2p/peer_graph_scope_tag
 - PEER_GRAPH_SCOPE
 - p2p/PEER_GRAPH_SCOPE
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
 - PEER_GRAPH_SCOPE
---

# PEER_GRAPH_SCOPE enumeration


## -description

The <b>PEER_GRAPH_SCOPE</b> enumeration specifies the network scope of a peer graph.

## -enum-fields

### -field PEER_GRAPH_SCOPE_ANY:0

The peer graph's network scope can contain any IP address, valid or otherwise.

### -field PEER_GRAPH_SCOPE_GLOBAL:1

The IP addresses for the peer graph's network scope can be from any unblocked address range.

### -field PEER_GRAPH_SCOPE_SITELOCAL:2

The IP addresses for the peer graph's network scope must be within the IP range defined for the site.

### -field PEER_GRAPH_SCOPE_LINKLOCAL:3

The IP addresses for the peer graph's network scope must be within the IP range defined for the local area network.

### -field PEER_GRAPH_SCOPE_LOOPBACK:4

The peer graph's network scope is the local computer's loopback IP address.

