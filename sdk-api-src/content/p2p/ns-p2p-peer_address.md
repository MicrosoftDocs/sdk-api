---
UID: NS:p2p.peer_address_tag
title: PEER_ADDRESS (p2p.h)
author: windows-sdk-content
description: The PEER_ADDRESS structure specifies the information about the IP address.
old-location: p2p\peer_address.htm
tech.root: P2PSdk
ms.assetid: 09476d3b-ec65-40a2-90ee-a20be230deca
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PPEER_ADDRESS, PEER_ADDRESS, PEER_ADDRESS structure [Peer Networking], PPEER_ADDRESS, PPEER_ADDRESS structure pointer [Peer Networking], p2p.peer_address, p2p/PPEER_ADDRESS, p2p/peer_address_tag"
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - P2P.h
api_name:
 - PEER_ADDRESS
product: Windows
targetos: Windows
req.typenames: PEER_ADDRESS, *PPEER_ADDRESS
req.redist: 
ms.custom: 19H1
---

# PEER_ADDRESS structure


## -description


The <b>PEER_ADDRESS</b> structure specifies the  information about the IP address.


## -struct-fields




### -field dwSize

Specifies the size of this structure.


### -field sin6

Specifies the IP address of the node in the Peer Infrastructure.


## -see-also




<a href="https://msdn.microsoft.com/039fa00e-c193-46fd-b7e6-41eb7baeab3e">PEER_CONNECTION_INFO</a>



<a href="https://msdn.microsoft.com/b8bd0e17-6af7-426d-ba38-11ff4948cf67">PEER_MEMBER</a>



<a href="https://msdn.microsoft.com/51cc6c27-91ca-4d02-95d6-207827450fd5">PEER_NODE_INFO</a>



<a href="https://msdn.microsoft.com/76a2c54d-4424-4aa3-9b62-3ebe88b63c9f">PeerGraphConnect</a>



<a href="https://msdn.microsoft.com/0625a2f6-7e16-43c7-8c03-1f0ddeda426f">PeerGraphOpenDirectConnection</a>



<a href="https://msdn.microsoft.com/a3c52754-91b0-4722-a459-87c70b3ab9ad">PeerGroupOpenDirectConnection</a>
 

 

