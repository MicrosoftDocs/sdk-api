---
UID: NS:winnt._SYSTEM_CPU_SET_INFORMATION
title: SYSTEM_CPU_SET_INFORMATION (winnt.h)
description: This structure is returned by GetSystemCpuSetInformation. It is used to enumerate the CPU Sets on the system and determine their current state.
helpviewer_keywords: ["*PSYSTEM_CPU_SET_INFORMATION","PSYSTEM_CPU_SET_INFORMATION","PSYSTEM_CPU_SET_INFORMATION structure pointer","SYSTEM_CPU_SET_INFORMATION","SYSTEM_CPU_SET_INFORMATION structure","base.system_cpu_set_information","winnt/PSYSTEM_CPU_SET_INFORMATION","winnt/SYSTEM_CPU_SET_INFORMATION"]
old-location: base\system_cpu_set_information.htm
tech.root: backup
ms.assetid: 48C38098-C42E-46D0-B938-CBD0BA7F8586
ms.date: 12/05/2018
ms.keywords: '*PSYSTEM_CPU_SET_INFORMATION, PSYSTEM_CPU_SET_INFORMATION, PSYSTEM_CPU_SET_INFORMATION structure pointer, SYSTEM_CPU_SET_INFORMATION, SYSTEM_CPU_SET_INFORMATION structure, base.system_cpu_set_information, winnt/PSYSTEM_CPU_SET_INFORMATION, winnt/SYSTEM_CPU_SET_INFORMATION'
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
req.typenames: SYSTEM_CPU_SET_INFORMATION, *PSYSTEM_CPU_SET_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SYSTEM_CPU_SET_INFORMATION
 - winnt/_SYSTEM_CPU_SET_INFORMATION
 - PSYSTEM_CPU_SET_INFORMATION
 - winnt/PSYSTEM_CPU_SET_INFORMATION
 - SYSTEM_CPU_SET_INFORMATION
 - winnt/SYSTEM_CPU_SET_INFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winnt.h
api_name:
 - SYSTEM_CPU_SET_INFORMATION
---

# SYSTEM_CPU_SET_INFORMATION structure


## -description

This structure is returned by <a href="/windows/desktop/ProcThread/getsystemcpusetinformation">GetSystemCpuSetInformation</a>. It is used to enumerate the CPU Sets on the system and determine their current state.

 This is a variable-sized structure designed for future expansion. When iterating over this structure, use the size field to determine the offset to the next structure.

## -struct-fields

### -field Size

This is the size, in bytes, of this information structure.

### -field Type

This is the type of information in the structure. Applications should skip any structures with unrecognized types.

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.CpuSet

### -field DUMMYUNIONNAME.CpuSet.Id

The ID of the specified CPU Set. This identifier can be used with <a href="/windows/desktop/ProcThread/setprocessdefaultcpusets">SetProcessDefaultCpuSets</a> or <a href="/windows/desktop/ProcThread/setthreadselectedcpusets">SetThreadSelectedCpuSets</a> when specifying a list of CPU Sets to affinitize to.

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

If set, the specified CPU Set is not available for general system use, but instead is allocated for exclusive use of some processes. If a non-NULL <b>Process</b> argument is specified in a call to <a href="/windows/desktop/ProcThread/getsystemcpusetinformation">GetSystemCpuSetInformation</a>, it is possible to determine if the processor is allocated for use with that process.


##### - CpuSet.AllocatedToTargetProcess : 1

This is set if the CPU Set is allocated for the exclusive use of some subset of the system processes and if it is allocated for the use of the process passed into <a href="/windows/desktop/ProcThread/getsystemcpusetinformation">GetSystemCpuSetInformation</a>.


##### - CpuSet.Parked : 1

If set, the home processor of this CPU Set is parked. If the CPU Set is on a parked processor, threads assigned to that set may be reassigned to other processors that are selected by the<b> Process Default</b> sets or the <b>Thread Selected</b> sets. If all such processors are parked, the threads are reassigned to other available processors on the system.


##### - CpuSet.RealTime : 1

This is set of the CPU Set is on a processor that is suitable for low-latency realtime processing.  The system takes steps to ensure that RealTime CPU Sets are unlikely to be running non-preemptible code, by moving other work like Interrupts and other application threads off of those processors.


##### - CpuSet.ReservedFlags : 4

Reserved.