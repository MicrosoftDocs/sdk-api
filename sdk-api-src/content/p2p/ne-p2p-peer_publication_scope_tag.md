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

# peer_publication_scope_tag enumeration


## -description


The <b>PEER_PUBLICATION_SCOPE</b> enumeration defines the set of scopes for the publication of peer objects or data.


## -enum-fields




### -field PEER_PUBLICATION_SCOPE_NONE

No scope is set for the publication of this data.


### -field PEER_PUBLICATION_SCOPE_NEAR_ME

The data is published to peers in the same logical or virtual subnet.


### -field PEER_PUBLICATION_SCOPE_INTERNET

The data is published to peers on the Internet.


### -field PEER_PUBLICATION_SCOPE_ALL

The data is published to all peers.


## -see-also




<a href="https://msdn.microsoft.com/f72e372a-0d23-47f4-8518-1296ec81ce55">Collaboration API Enumerations</a>
 

 

