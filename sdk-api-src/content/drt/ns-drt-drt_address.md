---
UID: NS:drt._DRT_ADDRESS
title: DRT_ADDRESS (drt.h)
description: DRT_ADDRESS structure contains endpoint information about a DRT node that participated in a search. This information is intended for use in debugging connectivity problems.
helpviewer_keywords: ["*PDRT_ADDRESS","DRT_ADDRESS","DRT_ADDRESS structure [Peer Networking]","PDRT_ADDRESS","PDRT_ADDRESS structure pointer [Peer Networking]","drt/DRT_ADDRESS","drt/PDRT_ADDRESS","p2p.drt_address"]
old-location: p2p\drt_address.htm
tech.root: p2p
ms.assetid: d6b00d5e-14f1-4e56-b8c8-f3936f6ae9fb
ms.date: 12/05/2018
ms.keywords: '*PDRT_ADDRESS, DRT_ADDRESS, DRT_ADDRESS structure [Peer Networking], PDRT_ADDRESS, PDRT_ADDRESS structure pointer [Peer Networking], drt/DRT_ADDRESS, drt/PDRT_ADDRESS, p2p.drt_address'
req.header: drt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: DRT_ADDRESS, *PDRT_ADDRESS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DRT_ADDRESS
 - drt/_DRT_ADDRESS
 - PDRT_ADDRESS
 - drt/PDRT_ADDRESS
 - DRT_ADDRESS
 - drt/DRT_ADDRESS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - drt.h
api_name:
 - DRT_ADDRESS
---

# DRT_ADDRESS structure


## -description

The <b>DRT_ADDRESS</b> structure contains endpoint information about a DRT node that participated in a search.  This information is intended for use in debugging connectivity problems.

## -struct-fields

### -field socketAddress

Contains the endpoint on which the DRT protocol is listening on the remote node.

### -field flags

Holds information explaining how this node behaved in the key lookup.

### -field nearness

Contains the number of bits that the key published by this node shares in common with the target key in the search.

### -field latency

Round trip time to this node.

## -see-also

<a href="/windows/desktop/api/drt/ns-drt-drt_address_list">DRT_ADDRESS_LIST</a>