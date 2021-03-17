---
UID: NF:p2p.PeerFreeData
title: PeerFreeData function (p2p.h)
description: The PeerFreeData function deallocates a block of data and returns it to the memory pool. Use the PeerFreeData function to free data that the Peer Identity Manager, Peer Grouping, and Peer Collaboration APIs return.
helpviewer_keywords: ["PeerFreeData","PeerFreeData function [Peer Networking]","p2p.peerfreedata","p2p/PeerFreeData"]
old-location: p2p\peerfreedata.htm
tech.root: p2p
ms.assetid: 54288829-c991-42d6-a7c4-874ed28dd106
ms.date: 12/05/2018
ms.keywords: PeerFreeData, PeerFreeData function [Peer Networking], p2p.peerfreedata, p2p/PeerFreeData
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
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PeerFreeData
 - p2p/PeerFreeData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - P2P.dll
api_name:
 - PeerFreeData
---

# PeerFreeData function


## -description

The <b>PeerFreeData</b> function deallocates a block of data and returns it to the memory pool. Use the <b>PeerFreeData</b> function to free  data that the Peer Identity Manager, Peer Grouping, and Peer Collaboration APIs return.

## -parameters

### -param pvData [in]

Pointer to a block of data to be deallocated. This parameter must reference a valid block of memory.

## -returns

There are no return values.

## -remarks

Do not use this function to release memory that the Peer Graphing API returns. Use <a href="/windows/desktop/api/p2p/nf-p2p-peergraphfreedata">PeerGraphFreeData</a> for memory that  the Peer Graphing API returns.

## -see-also

<a href="/windows/desktop/P2PSdk/grouping-api-functions">Grouping API
		  Functions</a>



<a href="/windows/desktop/P2PSdk/identity-manager-functions">Identity Manager Functions</a>