---
UID: NS:winnt._SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX
title: SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX (winnt.h)
description: Contains information about the relationships of logical processors and related hardware. The GetLogicalProcessorInformationEx function uses this structure.
helpviewer_keywords: ["*PSYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX","PSYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX","PSYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX structure pointer","RelationCache","RelationGroup","RelationNumaNode","RelationProcessorCore","RelationProcessorPackage","SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX","SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX structure","_SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX","base.system_logical_processor_information_ex","winnt/PSYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX","winnt/SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX"]
old-location: base\system_logical_processor_information_ex.htm
tech.root: backup
ms.assetid: 6ff16cda-c1dc-4d5c-ac60-756653cd6b07
ms.date: 27/02/2023
ms.keywords: '*PSYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX, PSYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX, PSYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX structure pointer, RelationCache, RelationGroup, RelationNumaNode, RelationProcessorCore, RelationProcessorPackage, RelationProcessorModule, RelationProcessorDie, SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX, SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX structure, _SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX, base.system_logical_processor_information_ex, winnt/PSYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX, winnt/SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX'
req.header: winnt.h
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
req.typenames: SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX, *PSYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX
 - winnt/_SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX
 - PSYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX
 - winnt/PSYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX
 - SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX
 - winnt/SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX
---

# SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX structure


## -description

Contains information about the relationships of logical processors and related hardware. The <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex">GetLogicalProcessorInformationEx</a> function uses this structure.

## -struct-fields

### -field Relationship

The type of relationship between the logical processors. This parameter can be one of the <a href="/windows/desktop/api/winnt/ne-winnt-logical_processor_relationship">LOGICAL_PROCESSOR_RELATIONSHIP</a> enumeration values.

### -field Size

The size of the structure.

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.Processor

A <a href="/windows/desktop/api/winnt/ns-winnt-processor_relationship">PROCESSOR_RELATIONSHIP</a> structure that describes processor affinity. This structure contains valid data only if the <b>Relationship</b> member is <b>RelationProcessorCore</b>, <b>RelationProcessorDie</b>, <b>RelationProcessorModule</b> or <b>RelationProcessorPackage</b>.

### -field DUMMYUNIONNAME.NumaNode

A <a href="/windows/desktop/api/winnt/ns-winnt-numa_node_relationship">NUMA_NODE_RELATIONSHIP</a> structure that describes a NUMA node. This structure contains valid data only if the <b>Relationship</b> member is <b>RelationNumaNode</b> or <b>RelationNumaNodeEx</b>.

### -field DUMMYUNIONNAME.Cache

A <a href="/windows/desktop/api/winnt/ns-winnt-cache_relationship">CACHE_RELATIONSHIP</a> structure that describes cache attributes. This structure contains valid data only if the <b>Relationship</b> member is <b>RelationCache</b>.

### -field DUMMYUNIONNAME.Group

A <a href="/windows/desktop/api/winnt/ns-winnt-group_relationship">GROUP_RELATIONSHIP</a> structure that contains information about the processor groups. This structure contains valid data only if the <b>Relationship</b> member is <b>RelationGroup</b>.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-cache_relationship">CACHE_RELATIONSHIP</a>



<a href="/windows/desktop/api/winnt/ns-winnt-group_relationship">GROUP_RELATIONSHIP</a>



<a href="/windows/desktop/api/winnt/ns-winnt-numa_node_relationship">NUMA_NODE_RELATIONSHIP</a>



<a href="/windows/desktop/api/winnt/ns-winnt-processor_relationship">PROCESSOR_RELATIONSHIP</a>
