---
UID: NS:p2p.peer_app_launch_info_tag
title: PEER_APP_LAUNCH_INFO (p2p.h)
description: The PEER_APP_LAUNCH_INFO structure contains the peer application application launch information provided by a contact in a previous peer invite request.
helpviewer_keywords: ["*PPEER_APP_LAUNCH_INFO","PCPEER_APP_LAUNCH_INFO","PCPEER_APP_LAUNCH_INFO structure pointer [Peer Networking]","PEER_APP_LAUNCH_INFO","PEER_APP_LAUNCH_INFO structure [Peer Networking]","PPEER_APP_LAUNCH_INFO","PPEER_APP_LAUNCH_INFO structure pointer [Peer Networking]","p2p.peer_app_launch_info","p2p/PCPEER_APP_LAUNCH_INFO","p2p/PEER_APP_LAUNCH_INFO","p2p/PPEER_APP_LAUNCH_INFO"]
old-location: p2p\peer_app_launch_info.htm
tech.root: p2p
ms.assetid: 98c7f7b8-438f-4ce3-86ab-0e824ff08dc4
ms.date: 12/05/2018
ms.keywords: '*PPEER_APP_LAUNCH_INFO, PCPEER_APP_LAUNCH_INFO, PCPEER_APP_LAUNCH_INFO structure pointer [Peer Networking], PEER_APP_LAUNCH_INFO, PEER_APP_LAUNCH_INFO structure [Peer Networking], PPEER_APP_LAUNCH_INFO, PPEER_APP_LAUNCH_INFO structure pointer [Peer Networking], p2p.peer_app_launch_info, p2p/PCPEER_APP_LAUNCH_INFO, p2p/PEER_APP_LAUNCH_INFO, p2p/PPEER_APP_LAUNCH_INFO'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PEER_APP_LAUNCH_INFO, *PPEER_APP_LAUNCH_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_app_launch_info_tag
 - p2p/peer_app_launch_info_tag
 - PPEER_APP_LAUNCH_INFO
 - p2p/PPEER_APP_LAUNCH_INFO
 - PEER_APP_LAUNCH_INFO
 - p2p/PEER_APP_LAUNCH_INFO
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
 - PEER_APP_LAUNCH_INFO
---

# PEER_APP_LAUNCH_INFO structure


## -description

The <b>PEER_APP_LAUNCH_INFO</b> structure contains the peer application application launch information provided by a contact in a previous peer invite request.

## -struct-fields

### -field pContact

Pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_contact">PEER_CONTACT</a> structure that contains information about the contact that sent the request to the local peer to launch the application referenced by the application.

### -field pEndpoint

Pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_endpoint">PEER_ENDPOINT</a> structure that contains information about the specific endpoint of the contact that sent the request to the local peer to launch the application referenced by the application

### -field pInvitation

Pointer to the <a href="/windows/desktop/api/p2p/ns-p2p-peer_invitation">PEER_INVITATION</a> structure that contains the invitation to launch a specific peer application application on the local peer.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_contact">PEER_CONTACT</a>



<a href="/windows/desktop/api/p2p/ns-p2p-peer_endpoint">PEER_ENDPOINT</a>



<a href="/windows/desktop/api/p2p/ns-p2p-peer_invitation">PEER_INVITATION</a>



<a href="/windows/desktop/P2PSdk/collaboration-api-structures">Peer Collaboration API Structures</a>