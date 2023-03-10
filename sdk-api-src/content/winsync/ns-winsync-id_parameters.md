---
UID: NS:winsync._ID_PARAMETERS
title: ID_PARAMETERS (winsync.h)
description: Represents the format schema for the group of IDs that are used to identify entities in a synchronization session.
helpviewer_keywords: ["ID_PARAMETERS","ID_PARAMETERS structure [Windows Sync]","winsync.id_parameters","winsync/ID_PARAMETERS"]
old-location: winsync\id_parameters.htm
tech.root: winsync
ms.assetid: 7391689a-5546-409a-9fff-2ceced1850fe
ms.date: 12/05/2018
ms.keywords: ID_PARAMETERS, ID_PARAMETERS structure [Windows Sync], winsync.id_parameters, winsync/ID_PARAMETERS
req.header: winsync.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ID_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ID_PARAMETERS
 - winsync/_ID_PARAMETERS
 - ID_PARAMETERS
 - winsync/ID_PARAMETERS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winsync.h
api_name:
 - ID_PARAMETERS
---

# ID_PARAMETERS structure


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

To obtain ID parameters, both providers are queried through a call to <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncprovider-getidparameters">ISyncProvider::GetIdParameters</a>. These ID parameters are then compared to verify that both providers use the same ID schema. If this verification fails, the synchronization session is not created, and an error code is returned.

## -see-also

<a href="/windows/desktop/api/winsync/ns-winsync-id_parameter_pair">ID_PARAMETER_PAIR Structure</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncprovider">ISyncProvider Interface</a>



<a href="/previous-versions/windows/desktop/winsync/windows-sync-structures">Windows Sync Structures</a>