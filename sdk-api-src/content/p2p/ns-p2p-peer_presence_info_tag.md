---
UID: NS:p2p.peer_presence_info_tag
title: peer_presence_info_tag
author: windows-sdk-content
description: The PEER_PRESENCE_INFO structure contains specific peer presence information.
old-location: p2p\peer_presence_info.htm
old-project: p2psdk
ms.assetid: e8f83ba8-81a3-4083-bc15-e00b2bec1cd4
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: "*PPEER_PRESENCE_INFO, PCPEER_PRESENCE_INFO, PCPEER_PRESENCE_INFO structure pointer [Peer Networking], PEER_PRESENCE_INFO, PEER_PRESENCE_INFO structure [Peer Networking], PPEER_PRESENCE_INFO, PPEER_PRESENCE_INFO structure pointer [Peer Networking], p2p.peer_presence_info, p2p/PCPEER_PRESENCE_INFO, p2p/PEER_PRESENCE_INFO, p2p/PPEER_PRESENCE_INFO, peer_presence_info_tag"
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
req.typenames: PEER_PRESENCE_INFO, *PPEER_PRESENCE_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - P2P.h
api_name:
 - PEER_PRESENCE_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# peer_presence_info_tag structure


## -description


The <b>PEER_PRESENCE_INFO</b> structure contains specific peer presence information.


## -struct-fields




### -field status


<a href="https://msdn.microsoft.com/0f7f6fa8-5da4-4f59-b9ea-0117ff8a3e28">PEER_PRESENCE_STATUS</a> enumeration value that indicates the current availability or level of participation by the peer in a peer collaboration network.


### -field pwzDescriptiveText

Zero-terminated Unicode string that contains a user- or application-defined message that expands upon the current status value. This string is limited to 255 characters.


## -remarks



Peer "presence" is information about a specific peer's level of participation in a peer collaboration network, such as whether or not the peer has logged into or out of the peer collaboration network, or has set a specific status (for example, "Busy, "Away").




## -see-also




<a href="https://msdn.microsoft.com/0f7f6fa8-5da4-4f59-b9ea-0117ff8a3e28">PEER_PRESENCE_STATUS</a>



<a href="https://msdn.microsoft.com/2634899c-3263-45ce-9fac-407e11e42cd4">Peer Collaboration API Structures</a>
 

 

