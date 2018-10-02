---
UID: NS:ntdsapi._DS_REPL_NEIGHBORSW
title: "_DS_REPL_NEIGHBORSW"
author: windows-sdk-content
description: The DS_REPL_NEIGHBORS structure is used with the DsReplicaGetInfo and DsReplicaGetInfo2 functions to provide inbound replication state data for naming context and source server pairs.
old-location: ad\ds_repl_neighbors.htm
tech.root: AD
ms.assetid: 1307399b-de29-43ec-97b4-05cd70c1a92d
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DS_REPL_NEIGHBORS, DS_REPL_NEIGHBORS structure [Active Directory], DS_REPL_NEIGHBORSW, _DS_REPL_NEIGHBORSW, _glines_ds_repl_neighbors, ad.ds__repl__neighbors, ad.ds_repl_neighbors, ntdsapi/DS_REPL_NEIGHBORS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
 - Ntdsapi.h
api_name:
 - DS_REPL_NEIGHBORS
product: Windows
targetos: Windows
req.typenames: DS_REPL_NEIGHBORSW
req.redist: 
---

# _DS_REPL_NEIGHBORSW structure


## -description


The <b>DS_REPL_NEIGHBORS</b> structure is used with the <a href="https://msdn.microsoft.com/b7ab22fe-ed92-4213-9b66-2dd5526286fa">DsReplicaGetInfo</a> and <a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a> functions to provide inbound replication state data for naming context and source server pairs.


## -struct-fields




### -field cNumNeighbors

Contains  the number of elements in the <b>rgNeighbor</b> array.


### -field dwReserved

Reserved for future use.


### -field rgNeighbor.size_is

 


### -field rgNeighbor.size_is.cNumNeighbors

 


### -field rgNeighbor

Contains an array of <a href="https://msdn.microsoft.com/acab74f4-5739-4310-895b-081062c0360b">DS_REPL_NEIGHBOR</a> structures that contain the requested replication data. The <b>cNumNeighbors</b> member contains the number of elements in this array.


## -see-also




<a href="https://msdn.microsoft.com/acab74f4-5739-4310-895b-081062c0360b">DS_REPL_NEIGHBOR</a>



<a href="https://msdn.microsoft.com/b7ab22fe-ed92-4213-9b66-2dd5526286fa">DsReplicaGetInfo</a>



<a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a>
 

 

