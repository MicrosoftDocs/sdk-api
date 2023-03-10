---
UID: NS:resapi._PaxosTagCStruct
title: PaxosTagCStruct (resapi.h)
description: Contains the Paxos tag values of a cluster node, which stores information about the cluster configuration version of the node when the cluster uses a File Share witness.
helpviewer_keywords: ["*PPaxosTagCStruct","PPaxosTagCStruct","PPaxosTagCStruct structure pointer [Failover Cluster]","PaxosTagCStruct","PaxosTagCStruct structure [Failover Cluster]","mscs.paxostagcstruct","resapi/PPaxosTagCStruct","resapi/PaxosTagCStruct"]
old-location: mscs\paxostagcstruct.htm
tech.root: MsCS
ms.assetid: 732CB125-F43A-4CC4-BC3F-EFB511BB7F2E
ms.date: 12/05/2018
ms.keywords: '*PPaxosTagCStruct, PPaxosTagCStruct, PPaxosTagCStruct structure pointer [Failover Cluster], PaxosTagCStruct, PaxosTagCStruct structure [Failover Cluster], mscs.paxostagcstruct, resapi/PPaxosTagCStruct, resapi/PaxosTagCStruct'
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
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
req.typenames: PaxosTagCStruct, *PPaxosTagCStruct
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PaxosTagCStruct
 - resapi/_PaxosTagCStruct
 - PPaxosTagCStruct
 - resapi/PPaxosTagCStruct
 - PaxosTagCStruct
 - resapi/PaxosTagCStruct
dev_langs:
 - c++
topic_type:
 - kbSyntax
api_type:
 - <TBD>
api_location:
api_name:
 - PaxosTagCStruct
---

# PaxosTagCStruct structure


## -description

Contains the Paxos tag values of a cluster node, which stores information about the cluster configuration version  of the node when the cluster uses a File Share witness.

## -struct-fields

### -field __padding__PaxosTagVtable

TBD

### -field __padding__NextEpochVtable

TBD

### -field __padding__NextEpoch_DateTimeVtable

TBD

### -field NextEpoch_DateTime_ticks

TBD

### -field NextEpoch_Value

The next epoch of the cluster configuration.

### -field __padding__BoundryNextEpoch

TBD

### -field __padding__EpochVtable

TBD

### -field __padding__Epoch_DateTimeVtable

TBD

### -field Epoch_DateTime_ticks

TBD

### -field Epoch_Value

The epoch of the cluster configuration.

### -field __padding__BoundryEpoch

TBD

### -field Sequence

The sequence of the cluster configuration.

### -field __padding__BoundrySequence

TBD

## -see-also

<a href="/previous-versions/windows/desktop/api/resapi/nf-resapi-resutilleftpaxosislessthanright">ResUtilLeftPaxosIsLessThanRight</a>



<a href="/previous-versions/windows/desktop/api/resapi/nf-resapi-resutilpaxoscomparer">ResUtilPaxosComparer</a>



<a href="/previous-versions/windows/desktop/mscs/resource-dll-structures">Resource DLL Structures</a>



<a href="/windows/desktop/api/resapi/ns-resapi-witnesstaghelper">WitnessTagHelper</a>



<a href="/windows/desktop/api/resapi/ns-resapi-witnesstagupdatehelper">WitnessTagUpdateHelper</a>