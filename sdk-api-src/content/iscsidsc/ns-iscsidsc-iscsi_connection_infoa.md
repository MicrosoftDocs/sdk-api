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

# ISCSI_CONNECTION_INFOA structure


## -description


The 	<b>ISCSI_CONNECTION_INFO</b> structure contains information about a connection.


## -struct-fields




### -field ConnectionId

A ISCSI_UNIQUE_CONNECTION_ID structure that contains the unique identifier for a connection. The LoginIScsiTarget and AddIScsiConnection functions return this value via the UniqueConnectionId parameter.


### -field InitiatorAddress

A string that represents the IP address of the initiator.


### -field TargetAddress

A string that represents the IP address of the target.


### -field InitiatorSocket

The socket number on the initiator that establishes the connection.


### -field TargetSocket

The socket number on the target that establishes the connection.


### -field CID

The connection identifier for the connection.


## -see-also




<a href="https://msdn.microsoft.com/cc68fda4-6dbf-42de-8e0e-e144bd4e9524">ISCSI_UNIQUE_CONNECTION_ID</a>
 

 

