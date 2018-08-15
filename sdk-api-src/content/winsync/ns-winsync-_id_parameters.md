---
UID: NS:winsync._ID_PARAMETERS
title: "_ID_PARAMETERS"
author: windows-sdk-content
description: Represents the format schema for the group of IDs that are used to identify entities in a synchronization session.
old-location: winsync\id_parameters.htm
old-project: winsync
ms.assetid: 7391689a-5546-409a-9fff-2ceced1850fe
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ID_PARAMETERS, ID_PARAMETERS structure [Windows Sync], _ID_PARAMETERS, winsync.id_parameters, winsync/ID_PARAMETERS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winsync.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: ID_PARAMETERS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winsync.h
api_name:
 - ID_PARAMETERS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
 

 

