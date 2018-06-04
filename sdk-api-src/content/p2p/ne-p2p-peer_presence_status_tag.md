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

# peer_presence_status_tag enumeration


## -description


The <b>PEER_PRESENCE_STATUS</b> enumeration defines the set of possible presence status settings available to a peer that participates in a peer collaboration network. These settings can be set by a peer collaboration network endpoint to indicate the peer's current level of participation to its watchers.


## -enum-fields




### -field PEER_PRESENCE_OFFLINE

The user is offline.


### -field PEER_PRESENCE_OUT_TO_LUNCH

The user is currently "out to lunch" and unable to respond.


### -field PEER_PRESENCE_AWAY

The user is away and unable to respond.


### -field PEER_PRESENCE_BE_RIGHT_BACK

The user has stepped away from the application and will participate soon.


### -field PEER_PRESENCE_IDLE

The user is idling.


### -field PEER_PRESENCE_BUSY

The user is busy and does not wish to be disturbed.


### -field PEER_PRESENCE_ON_THE_PHONE

The user is currently on the phone and does not wish to be disturbed.


### -field PEER_PRESENCE_ONLINE

The user is actively participating in the peer collaboration network.


## -see-also




<a href="https://msdn.microsoft.com/f72e372a-0d23-47f4-8518-1296ec81ce55">Collaboration API Enumerations</a>
 

 

