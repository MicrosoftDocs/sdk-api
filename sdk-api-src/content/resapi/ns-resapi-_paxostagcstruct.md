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
 

 

