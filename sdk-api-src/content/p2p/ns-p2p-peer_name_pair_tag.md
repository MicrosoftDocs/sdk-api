---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# peer_name_pair_tag structure


## -description


The <b>PEER_NAME_PAIR</b> structure contains the results of a call to  <a href="https://msdn.microsoft.com/015faeb3-82d9-49e5-a451-7394bf83240f">PeerGetNextItem</a>.


## -struct-fields




### -field dwSize

Specifies the size, in bytes, of this structure.


### -field pwzPeerName

Specifies the peer name of the peer identity or peer group.


### -field pwzFriendlyName

Specifies the friendly name of the peer identity or peer group.


## -remarks



This structure is used when enumerating peer identities and peer groups associated with a specific identity.

When enumerating peer identities, each <b>PEER_NAME_PAIR</b> structure contains a peer name and the friendly name of the identity.

When enumerating peer groups,  each <b>PEER_NAME_PAIR</b>  structure contains the peer name and friendly name of the corresponding peer group.




## -see-also




<a href="https://msdn.microsoft.com/debb3c57-b5d2-440b-acf2-b6d8e712849b">PeerEnumGroups</a>



<a href="https://msdn.microsoft.com/91f18185-0292-41a3-8aff-8b345cab5e82">PeerEnumIdentities</a>



<a href="https://msdn.microsoft.com/015faeb3-82d9-49e5-a451-7394bf83240f">PeerGetNextItem</a>
 

 

