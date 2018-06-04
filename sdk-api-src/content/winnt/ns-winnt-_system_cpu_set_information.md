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

# _SYSTEM_CPU_SET_INFORMATION structure


## -description


This structure is returned by <a href="https://msdn.microsoft.com/168B00AB-1B11-44A0-B548-903CA3F4BBDE">GetSystemCpuSetInformation</a>. It is used to enumerate the CPU Sets on the system and determine their current state.

 This is a variable-sized structure designed for future expansion. When iterating over this structure, use the size field to determine the offset to the next structure.


## -struct-fields




### -field Size

This is the size, in bytes, of this information structure.


### -field Type

This is the type of information in the structure. Applications should skip any structures with unrecognized types.


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.CpuSet


### -field DUMMYUNIONNAME.CpuSet.Id

The ID of the specified CPU Set. This identifier can be used with <a href="https://msdn.microsoft.com/7A510A8D-B06C-4B7B-9A87-BCFE0DE4D17B">SetProcessDefaultCpuSets</a> or <a href="https://msdn.microsoft.com/A73F7118-CC4A-45E6-869A-DFF6924D10C8">SetThreadSelectedCpuSets</a> when specifying a list of CPU Sets to affinitize to.


### -field DUMMYUNIONNAME.CpuSet.Group

Specifies the Processor Group of the CPU Set. All other values in the CpuSet structure are relative to the processor group.


### -field DUMMYUNIONNAME.CpuSet.LogicalProcessorIndex

Specifies the group-relative index of the home processor of the CPU Set. Unless the CPU Set is parked for thermal or power management reasons or assigned for exclusive use to another application, threads will run on the home processor of one of their CPU Sets. The <b>Group</b> and <b>LogicalProcessorIndex</b> fields are the same as the ones found in the PROCESSOR_NUMBER structure and they correspond to the <b>Group</b> field and <b>Mask</b> field of the GROUP_AFFINITY structure.


### -field DUMMYUNIONNAME.CpuSet.CoreIndex

A group-relative value indicating which "Core" has the home processor of the CPU Set. This number is the same for all CPU Sets in the same group that share significant execution resources with each other, such as different hardware threads on a single core that supports simultaneous multi-threading.


### -field DUMMYUNIONNAME.CpuSet.LastLevelCacheIndex

A group-relative value indicating which CPU Sets share at least one level of cache with each other. This value is the same for all CPU Sets in a group that are on processors that share cache with each other.


### -field DUMMYUNIONNAME.CpuSet.NumaNodeIndex

A group-relative value indicating which NUMA node a CPU Set is on. All CPU Sets in a given group that are on the same NUMA node will have the same value for this field.


### -field DUMMYUNIONNAME.CpuSet.EfficiencyClass

 A value indicating the intrinsic energy efficiency of a processor for systems that support heterogeneous processors (such as ARM big.LITTLE systems). CPU Sets with higher numerical values of this field have home processors that are faster but less power-efficient than ones with lower values.


### -field DUMMYUNIONNAME.CpuSet.DUMMYUNIONNAME2

 


### -field DUMMYUNIONNAME.CpuSet.DUMMYUNIONNAME2.AllFlags

 


### -field DUMMYUNIONNAME.CpuSet.DUMMYUNIONNAME2.DUMMYSTRUCTNAME

 


### -field DUMMYUNIONNAME.CpuSet.DUMMYUNIONNAME2.DUMMYSTRUCTNAME.Parked

 


### -field DUMMYUNIONNAME.CpuSet.DUMMYUNIONNAME2.DUMMYSTRUCTNAME.Allocated

 


### -field DUMMYUNIONNAME.CpuSet.DUMMYUNIONNAME2.DUMMYSTRUCTNAME.AllocatedToTargetProcess

 


### -field DUMMYUNIONNAME.CpuSet.DUMMYUNIONNAME2.DUMMYSTRUCTNAME.RealTime

 


### -field DUMMYUNIONNAME.CpuSet.DUMMYUNIONNAME2.DUMMYSTRUCTNAME.ReservedFlags

 


### -field DUMMYUNIONNAME.CpuSet.Reserved

Reserved.


### -field DUMMYUNIONNAME.CpuSet.SchedulingClass

 


### -field DUMMYUNIONNAME.CpuSet.AllocationTag

Specifies a tag used by Core Allocation to communicate a given allocated CPU Set between threads in different components.


##### - CpuSet.Allocated : 1

If set, the specified CPU Set is not available for general system use, but instead is allocated for exclusive use of some processes. If a non-NULL <b>Process</b> argument is specified in a call to <a href="https://msdn.microsoft.com/168B00AB-1B11-44A0-B548-903CA3F4BBDE">GetSystemCpuSetInformation</a>, it is possible to determine if the processor is allocated for use with that process.


##### - CpuSet.AllocatedToTargetProcess : 1

This is set if the CPU Set is allocated for the exclusive use of some subset of the system processes and if it is allocated for the use of the process passed into <a href="https://msdn.microsoft.com/168B00AB-1B11-44A0-B548-903CA3F4BBDE">GetSystemCpuSetInformation</a>.


##### - CpuSet.Parked : 1

If set, the home processor of this CPU Set is parked. If the CPU Set is on a parked processor, threads assigned to that set may be reassigned to other processors that are selected by the<b> Process Default</b> sets or the <b>Thread Selected</b> sets. If all such processors are parked, the threads are reassigned to other available processors on the system.


##### - CpuSet.RealTime : 1

This is set of the CPU Set is on a processor that is suitable for low-latency realtime processing.  The system takes steps to ensure that RealTime CPU Sets are unlikely to be running non-preemptible code, by moving other work like Interrupts and other application threads off of those processors.


##### - CpuSet.ReservedFlags : 4

Reserved.

