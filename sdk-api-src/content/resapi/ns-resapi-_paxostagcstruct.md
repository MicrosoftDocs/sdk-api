---
UID: NS:resapi._PaxosTagCStruct
title: "_PaxosTagCStruct"
author: windows-driver-content
description: Contains the Paxos tag values of a cluster node, which stores information about the cluster configuration version of the node when the cluster uses a File Share witness.
old-location: mscs\paxostagcstruct.htm
old-project: MsCS
ms.assetid: 732CB125-F43A-4CC4-BC3F-EFB511BB7F2E
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: "*PPaxosTagCStruct, PPaxosTagCStruct, PPaxosTagCStruct structure pointer [Failover Cluster], PaxosTagCStruct, PaxosTagCStruct structure [Failover Cluster], _PaxosTagCStruct, mscs.paxostagcstruct, resapi/PPaxosTagCStruct, resapi/PaxosTagCStruct"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: PaxosTagCStruct, *PPaxosTagCStruct
topic_type:
-	kbSyntax
api_type:
-	<TBD>
api_location:
-
api_name:
-	PaxosTagCStruct
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# _PaxosTagCStruct structure


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




<a href="https://msdn.microsoft.com/01CBFC67-02D0-439D-BE4E-EA0A2448FDEE">ResUtilLeftPaxosIsLessThanRight</a>



<a href="https://msdn.microsoft.com/414F9BB0-2490-43A9-BE38-877B283573E1">ResUtilPaxosComparer</a>



<a href="https://msdn.microsoft.com/9ab4b974-28b5-4f33-a7c4-b9b2472059aa">Resource DLL Structures</a>



<a href="https://msdn.microsoft.com/FFE7EF63-4025-4CC5-B3F8-FF07FA67AFD1">WitnessTagHelper</a>



<a href="https://msdn.microsoft.com/4737A2B0-E295-49B6-8A84-D38BC317011B">WitnessTagUpdateHelper</a>
 

 

