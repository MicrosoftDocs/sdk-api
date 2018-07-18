---
UID: NS:p2p.peer_app_launch_info_tag
title: peer_app_launch_info_tag
author: windows-sdk-content
description: The PEER_APP_LAUNCH_INFO structure contains the peer application application launch information provided by a contact in a previous peer invite request.
old-location: p2p\peer_app_launch_info.htm
old-project: P2PSdk
ms.assetid: 98c7f7b8-438f-4ce3-86ab-0e824ff08dc4
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: "*PPEER_APP_LAUNCH_INFO, PCPEER_APP_LAUNCH_INFO, PCPEER_APP_LAUNCH_INFO structure pointer [Peer Networking], PEER_APP_LAUNCH_INFO, PEER_APP_LAUNCH_INFO structure [Peer Networking], PPEER_APP_LAUNCH_INFO, PPEER_APP_LAUNCH_INFO structure pointer [Peer Networking], p2p.peer_app_launch_info, p2p/PCPEER_APP_LAUNCH_INFO, p2p/PEER_APP_LAUNCH_INFO, p2p/PPEER_APP_LAUNCH_INFO, peer_app_launch_info_tag"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: PEER_APP_LAUNCH_INFO, *PPEER_APP_LAUNCH_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - P2P.h
api_name:
 - PEER_APP_LAUNCH_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# peer_app_launch_info_tag structure


## -description


The <b>PEER_APP_LAUNCH_INFO</b> structure contains the peer application application launch information provided by a contact in a previous peer invite request.


## -struct-fields




### -field pContact

Pointer to a <a href="https://msdn.microsoft.com/b84a17fc-35d6-4098-9bb3-18e708541a80">PEER_CONTACT</a> structure that contains information about the contact that sent the request to the local peer to launch the application referenced by the application.


### -field pEndpoint

Pointer to a <a href="https://msdn.microsoft.com/9687b332-14ed-4023-b8c2-437d75fd0298">PEER_ENDPOINT</a> structure that contains information about the specific endpoint of the contact that sent the request to the local peer to launch the application referenced by the application


### -field pInvitation

Pointer to the <a href="https://msdn.microsoft.com/b74b45c0-760f-4008-87dd-9fdea0d4be05">PEER_INVITATION</a> structure that contains the invitation to launch a specific peer application application on the local peer.


## -see-also




<a href="https://msdn.microsoft.com/b84a17fc-35d6-4098-9bb3-18e708541a80">PEER_CONTACT</a>



<a href="https://msdn.microsoft.com/9687b332-14ed-4023-b8c2-437d75fd0298">PEER_ENDPOINT</a>



<a href="https://msdn.microsoft.com/b74b45c0-760f-4008-87dd-9fdea0d4be05">PEER_INVITATION</a>



<a href="https://msdn.microsoft.com/2634899c-3263-45ce-9fac-407e11e42cd4">Peer Collaboration API Structures</a>
 

 

