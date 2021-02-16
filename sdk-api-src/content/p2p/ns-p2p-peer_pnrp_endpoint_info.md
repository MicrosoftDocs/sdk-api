---
UID: NS:p2p.peer_pnrp_endpoint_info_tag
title: PEER_PNRP_ENDPOINT_INFO (p2p.h)
description: Contains the IP addresses and data associated with a peer endpoint.
helpviewer_keywords: ["*PPEER_PNRP_ENDPOINT_INFO","PEER_PNRP_ENDPOINT_INFO","PEER_PNRP_ENDPOINT_INFO structure [Peer Networking]","PPEER_PNRP_ENDPOINT_INFO","PPEER_PNRP_ENDPOINT_INFO structure pointer [Peer Networking]","p2p.peer_pnrp_endpoint_info","p2p/PEER_PNRP_ENDPOINT_INFO","p2p/PPEER_PNRP_ENDPOINT_INFO"]
old-location: p2p\peer_pnrp_endpoint_info.htm
tech.root: p2p
ms.assetid: 986e3bec-9915-4a7c-8f54-faf25fa2848c
ms.date: 12/05/2018
ms.keywords: '*PPEER_PNRP_ENDPOINT_INFO, PEER_PNRP_ENDPOINT_INFO, PEER_PNRP_ENDPOINT_INFO structure [Peer Networking], PPEER_PNRP_ENDPOINT_INFO, PPEER_PNRP_ENDPOINT_INFO structure pointer [Peer Networking], p2p.peer_pnrp_endpoint_info, p2p/PEER_PNRP_ENDPOINT_INFO, p2p/PPEER_PNRP_ENDPOINT_INFO'
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only],Windows XP with SP1 with the Advanced Networking Pack for Windows XP
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: PEER_PNRP_ENDPOINT_INFO, *PPEER_PNRP_ENDPOINT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_pnrp_endpoint_info_tag
 - p2p/peer_pnrp_endpoint_info_tag
 - PPEER_PNRP_ENDPOINT_INFO
 - p2p/PPEER_PNRP_ENDPOINT_INFO
 - PEER_PNRP_ENDPOINT_INFO
 - p2p/PEER_PNRP_ENDPOINT_INFO
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
 - PEER_PNRP_ENDPOINT_INFO
---

# PEER_PNRP_ENDPOINT_INFO structure


## -description

The <b>PEER_PNRP_ENDPOINT_INFO</b> structure contains the IP addresses and data associated with a peer endpoint.

## -struct-fields

### -field pwzPeerName

The peer name associated with this peer endpoint.

### -field cAddresses

The number of SOCKADDR structures in <b>pAddresses</b>.

### -field ppAddresses

Pointer to an array of pointers to SOCKADDR structures that contain the IP addresses for the peer endpoint's network interface.

### -field pwzComment

Pointer to a zero-terminated Unicode string that contains a comment for this peer endpoint.

### -field payload

Pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_data">PEER_DATA</a> structure that contains application-specific data for the peer endpoint (such as a message or an image).