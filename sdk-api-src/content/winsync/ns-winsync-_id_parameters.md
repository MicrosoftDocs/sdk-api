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

# _ID_PARAMETERS structure


## -description


Represents the format schema for the group of IDs that are used to identify entities in a synchronization session.


## -struct-fields




### -field dwSize

The number of bytes in the <b>ID_PARAMETERS</b> structure.


### -field replicaId

The ID format that is expected for replica IDs.


### -field itemId

The ID format that is expected for item IDs.


### -field changeUnitId

The ID format that is expected for change unit IDs.


## -remarks



To obtain ID parameters, both providers are queried through a call to <a href="https://msdn.microsoft.com/a1839c53-7978-4a14-8b17-43621b801f13">ISyncProvider::GetIdParameters</a>. These ID parameters are then compared to verify that both providers use the same ID schema. If this verification fails, the synchronization session is not created, and an error code is returned.




## -see-also




<a href="https://msdn.microsoft.com/f2b47196-8112-4f04-9944-a4a686d3c25c">ID_PARAMETER_PAIR Structure</a>



<a href="https://msdn.microsoft.com/0664267f-90ba-4123-bfe5-7cf748b78c10">ISyncProvider Interface</a>



<a href="https://msdn.microsoft.com/eed33384-f8bd-4a3a-8d04-b59c534f9114">Windows Sync Structures</a>
 

 

