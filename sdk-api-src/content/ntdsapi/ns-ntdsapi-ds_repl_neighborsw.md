---
UID: NS:ntdsapi._DS_REPL_NEIGHBORSW
title: DS_REPL_NEIGHBORSW (ntdsapi.h)
description: The DS_REPL_NEIGHBORS structure is used with the DsReplicaGetInfo and DsReplicaGetInfo2 functions to provide inbound replication state data for naming context and source server pairs.
helpviewer_keywords: ["DS_REPL_NEIGHBORS","DS_REPL_NEIGHBORS structure [Active Directory]","DS_REPL_NEIGHBORSW","_DS_REPL_NEIGHBORSW","_glines_ds_repl_neighbors","ad.ds__repl__neighbors","ad.ds_repl_neighbors","ntdsapi/DS_REPL_NEIGHBORS"]
old-location: ad\ds_repl_neighbors.htm
tech.root: ad
ms.assetid: 1307399b-de29-43ec-97b4-05cd70c1a92d
ms.date: 12/05/2018
ms.keywords: DS_REPL_NEIGHBORS, DS_REPL_NEIGHBORS structure [Active Directory], DS_REPL_NEIGHBORSW, _DS_REPL_NEIGHBORSW, _glines_ds_repl_neighbors, ad.ds__repl__neighbors, ad.ds_repl_neighbors, ntdsapi/DS_REPL_NEIGHBORS
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
targetos: Windows
req.typenames: DS_REPL_NEIGHBORSW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DS_REPL_NEIGHBORSW
 - ntdsapi/_DS_REPL_NEIGHBORSW
 - DS_REPL_NEIGHBORSW
 - ntdsapi/DS_REPL_NEIGHBORSW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntdsapi.h
api_name:
 - DS_REPL_NEIGHBORS
---

# DS_REPL_NEIGHBORSW structure


## -description

The <b>DS_REPL_NEIGHBORS</b> structure is used with the <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfow">DsReplicaGetInfo</a> and <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfo2w">DsReplicaGetInfo2</a> functions to provide inbound replication state data for naming context and source server pairs.

## -struct-fields

### -field cNumNeighbors

Contains  the number of elements in the <b>rgNeighbor</b> array.

### -field dwReserved

Reserved for future use.

### -field rgNeighbor.size_is

### -field rgNeighbor.size_is.cNumNeighbors

### -field rgNeighbor

Contains an array of <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_neighborw">DS_REPL_NEIGHBOR</a> structures that contain the requested replication data. The <b>cNumNeighbors</b> member contains the number of elements in this array.

## -see-also

<a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_neighborw">DS_REPL_NEIGHBOR</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfow">DsReplicaGetInfo</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfo2w">DsReplicaGetInfo2</a>