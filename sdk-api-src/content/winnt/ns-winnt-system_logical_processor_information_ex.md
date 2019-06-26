---
UID: NS:winnt._SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX
title: SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX (winnt.h)
author: windows-sdk-content
description: Contains information about the relationships of logical processors and related hardware. The GetLogicalProcessorInformationEx function uses this structure.
old-location: base\system_logical_processor_information_ex.htm
tech.root: ProcThread
ms.assetid: 6ff16cda-c1dc-4d5c-ac60-756653cd6b07
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PSYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX, PSYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX, PSYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX structure pointer, RelationCache, RelationGroup, RelationNumaNode, RelationProcessorCore, RelationProcessorPackage, SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX, SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX structure, _SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX, base.system_logical_processor_information_ex, winnt/PSYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX, winnt/SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX"
ms.topic: struct
f1_keywords: 
 - "winnt/SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX
product: Windows
targetos: Windows
req.typenames: SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX, *PSYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX
req.redist: 
ms.custom: 19H1
---

# SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX structure


## -description


Contains information about the relationships of logical processors and related hardware. The <a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex">GetLogicalProcessorInformationEx</a> function uses this structure.


## -struct-fields




### -field Relationship

The type of relationship between the logical processors. This parameter can be one of the following <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ne-winnt-_logical_processor_relationship">LOGICAL_PROCESSOR_RELATIONSHIP</a> values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RelationCache"></a><a id="relationcache"></a><a id="RELATIONCACHE"></a><dl>
<dt><b>RelationCache</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The specified logical processors  share a cache. The <b>Cache</b> member contains additional information.

</td>
</tr>
<tr>
<td width="40%"><a id="RelationGroup"></a><a id="relationgroup"></a><a id="RELATIONGROUP"></a><dl>
<dt><b>RelationGroup</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The specified logical processors share a processor group. The <b>Group</b> member contains additional information.

</td>
</tr>
<tr>
<td width="40%"><a id="RelationNumaNode"></a><a id="relationnumanode"></a><a id="RELATIONNUMANODE"></a><dl>
<dt><b>RelationNumaNode</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The specified logical processors  are part of the same NUMA node. The <b>NumaNode</b> member  contains additional information.

</td>
</tr>
<tr>
<td width="40%"><a id="RelationProcessorCore"></a><a id="relationprocessorcore"></a><a id="RELATIONPROCESSORCORE"></a><dl>
<dt><b>RelationProcessorCore</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The specified logical processors share a single processor core. The <b>Processor</b> member contains additional information.

</td>
</tr>
<tr>
<td width="40%"><a id="RelationProcessorPackage"></a><a id="relationprocessorpackage"></a><a id="RELATIONPROCESSORPACKAGE"></a><dl>
<dt><b>RelationProcessorPackage</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The specified logical processors share a physical package. The <b>Processor</b> member contains additional information.

</td>
</tr>
</table>
 


### -field Size

The size of the structure.


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.Processor

A <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_processor_relationship">PROCESSOR_RELATIONSHIP</a> structure that describes processor affinity. This structure contains valid data only if the <b>Relationship</b> member is <b>RelationProcessorCore</b> or <b>RelationProcessorPackage</b>.


### -field DUMMYUNIONNAME.NumaNode

A <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_numa_node_relationship">NUMA_NODE_RELATIONSHIP</a> structure that describes a NUMA node. This structure contains valid data only if the <b>Relationship</b> member is <b>RelationNumaNode</b>.


### -field DUMMYUNIONNAME.Cache

A <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_cache_relationship">CACHE_RELATIONSHIP</a> structure that describes cache attributes. This structure contains valid data only if the <b>Relationship</b> member is <b>RelationCache</b>.


### -field DUMMYUNIONNAME.Group

A <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_group_relationship">GROUP_RELATIONSHIP</a> structure that contains information about the processor groups. This structure contains valid data only if the <b>Relationship</b> member is <b>RelationGroup</b>.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_cache_relationship">CACHE_RELATIONSHIP</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_group_relationship">GROUP_RELATIONSHIP</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_numa_node_relationship">NUMA_NODE_RELATIONSHIP</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_processor_relationship">PROCESSOR_RELATIONSHIP</a>
 

 

