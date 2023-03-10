---
UID: NF:p2p.PeerGraphFreeData
title: PeerGraphFreeData function (p2p.h)
description: The PeerGraphFreeData function frees resources that several of the Peer Graphing API functions return.
helpviewer_keywords: ["PeerGraphFreeData","PeerGraphFreeData function [Peer Networking]","p2p.peergraphfreedata","p2p/PeerGraphFreeData"]
old-location: p2p\peergraphfreedata.htm
tech.root: p2p
ms.assetid: a5b7d563-214a-48e0-b184-0c12d62fb125
ms.date: 12/05/2018
ms.keywords: PeerGraphFreeData, PeerGraphFreeData function [Peer Networking], p2p.peergraphfreedata, p2p/PeerGraphFreeData
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
req.lib: P2PGraph.lib
req.dll: P2PGraph.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PeerGraphFreeData
 - p2p/PeerGraphFreeData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - P2PGraph.dll
api_name:
 - PeerGraphFreeData
---

# PeerGraphFreeData function


## -description

The <b>PeerGraphFreeData</b> function frees resources that several of the Peer Graphing API functions return.

## -parameters

### -param pvData [in]

Pointer to an item to free.

## -returns

This function does not have return values.

## -remarks

The [PEER_RECORD](./ns-p2p-peer_record.md).

## -see-also

<a href="/windows/desktop/api/p2p/nf-p2p-peergraphgeteventdata">PeerGraphGetEventData</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphgetnextitem">PeerGraphGetNextItem</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphgetnodeinfo">PeerGraphGetNodeInfo</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphgetproperties">PeerGraphGetProperties</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphgetrecord">PeerGraphGetRecord</a>