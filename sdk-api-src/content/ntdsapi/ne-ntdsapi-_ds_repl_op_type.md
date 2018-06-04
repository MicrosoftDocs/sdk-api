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

# _DS_REPL_OP_TYPE enumeration


## -description


The <b>DS_REPL_OP_TYPE</b> enumeration type is used to indicate the type of replication operation that a given entry in the replication queue represents.


## -enum-fields




### -field DS_REPL_OP_TYPE_SYNC

Indicates an inbound replication over an existing replication agreement from a direct replication partner.


### -field DS_REPL_OP_TYPE_ADD

Indicates the addition of a replication agreement for a new direct replication partner.


### -field DS_REPL_OP_TYPE_DELETE

Indicates the removal of a replication agreement for an existing direct replication partner.


### -field DS_REPL_OP_TYPE_MODIFY

Indicates the modification of a replication agreement for an existing direct replication partner.


### -field DS_REPL_OP_TYPE_UPDATE_REFS

Indicates the addition, deletion, or update of outbound change notification data for a direct replication partner.


## -see-also




<a href="https://msdn.microsoft.com/eafa3285-4474-4077-a6ad-b37f8211e7e6">Active Directory Enumerations</a>



<a href="https://msdn.microsoft.com/b7ab22fe-ed92-4213-9b66-2dd5526286fa">DsReplicaGetInfo</a>



<a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a>
 

 

