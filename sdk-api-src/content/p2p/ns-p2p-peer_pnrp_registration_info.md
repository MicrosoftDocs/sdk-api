---
UID: NS:p2p.peer_pnrp_registration_info_tag
title: PEER_PNRP_REGISTRATION_INFO (p2p.h)
description: Contains the information provided by a peer identity when it registers with a PNRP cloud.
helpviewer_keywords: ["*PPEER_PNRP_REGISTRATION_INFO","PEER_PNRP_REGISTRATION_INFO","PEER_PNRP_REGISTRATION_INFO structure [Peer Networking]","PPEER_PNRP_REGISTRATION_INFO","PPEER_PNRP_REGISTRATION_INFO structure pointer [Peer Networking]","p2p.peer_pnrp_registration_info","p2p/PEER_PNRP_REGISTRATION_INFO","p2p/PPEER_PNRP_REGISTRATION_INFO"]
old-location: p2p\peer_pnrp_registration_info.htm
tech.root: p2p
ms.assetid: 2825cb65-94b4-4bed-acff-7fa35a992284
ms.date: 12/05/2018
ms.keywords: '*PPEER_PNRP_REGISTRATION_INFO, PEER_PNRP_REGISTRATION_INFO, PEER_PNRP_REGISTRATION_INFO structure [Peer Networking], PPEER_PNRP_REGISTRATION_INFO, PPEER_PNRP_REGISTRATION_INFO structure pointer [Peer Networking], p2p.peer_pnrp_registration_info, p2p/PEER_PNRP_REGISTRATION_INFO, p2p/PPEER_PNRP_REGISTRATION_INFO'
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
req.typenames: PEER_PNRP_REGISTRATION_INFO, *PPEER_PNRP_REGISTRATION_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_pnrp_registration_info_tag
 - p2p/peer_pnrp_registration_info_tag
 - PPEER_PNRP_REGISTRATION_INFO
 - p2p/PPEER_PNRP_REGISTRATION_INFO
 - PEER_PNRP_REGISTRATION_INFO
 - p2p/PEER_PNRP_REGISTRATION_INFO
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
 - PEER_PNRP_REGISTRATION_INFO
---

# PEER_PNRP_REGISTRATION_INFO structure


## -description

The <b>PEER_PNRP_REGISTRATION_INFO</b> structure contains the information provided by a peer identity when it registers with a PNRP cloud.

## -struct-fields

### -field pwzCloudName

Pointer to a Unicode string that contains the name of the PNRP cloud for which this peer identity is requesting registration. If <b>NULL</b>, the registration will be made in all clouds.  It is possible to use the special value PEER_PNRP_ALL_LINK_CLOUDS to register in all link local clouds.

### -field pwzPublishingIdentity

Pointer to a Unicode string that contains the name of the peer identity requesting registration.

### -field cAddresses

The number of SOCKADDR structures in <b>ppAddresses</b>. It is possible to use the special value PEER_PNRP_AUTO_ADDRESSES to have the infrastructure automatically choose addresses.

### -field ppAddresses

Pointer to an array of pointers to SOCKADDR structures that contain the IP addresses bound to the network interface of the peer identity requesting registration.

### -field wPort

The network interface port assigned to the address that the peer is publishing.

### -field pwzComment

Pointer to a zero-terminated Unicode string that contains a comment for this peer endpoint.

### -field payload

A <a href="/windows/desktop/api/p2p/ns-p2p-peer_data">PEER_DATA</a> structure that contains a pointer to an opaque byte buffer containing application-specific data for the peer endpoint (such as a message or an image).