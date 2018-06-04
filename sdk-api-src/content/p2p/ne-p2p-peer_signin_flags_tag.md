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

# peer_signin_flags_tag enumeration


## -description


The <b>PEER_SIGNIN_FLAGS</b> enumeration defines the set of peer presence publication behaviors available when the peer signs in to a peer collaboration network.


## -enum-fields




### -field PEER_SIGNIN_NONE

A peer's presence is not being published in any scope.


### -field PEER_SIGNIN_NEAR_ME

The peer can publish availability information to endpoints in the same subnet or local area network, or query for other endpoints available on the subnet.


### -field PEER_SIGNIN_INTERNET

The peer can publish presence, applications, and objects to all contacts in a peer's contact list.



### -field PEER_SIGNIN_ALL

The peer can publish presence, applications, and objects to all contacts in a peer's contact list, or query for other endpoints available on the subnet.


## -see-also




<a href="https://msdn.microsoft.com/f72e372a-0d23-47f4-8518-1296ec81ce55">Collaboration API Enumerations</a>
 

 

