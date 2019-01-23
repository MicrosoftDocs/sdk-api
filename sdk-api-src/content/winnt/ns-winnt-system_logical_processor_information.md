---
UID: NS:winnt._SYSTEM_LOGICAL_PROCESSOR_INFORMATION
title: SYSTEM_LOGICAL_PROCESSOR_INFORMATION
author: windows-sdk-content
description: Describes the relationship between the specified processor set. This structure is used with the GetLogicalProcessorInformation function.
old-location: base\system_logical_processor_information.htm
tech.root: procthread
ms.assetid: 32ef5dd8-c00d-44ee-a291-a18653beb1b9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PSYSTEM_LOGICAL_PROCESSOR_INFORMATION, PSYSTEM_LOGICAL_PROCESSOR_INFORMATION, PSYSTEM_LOGICAL_PROCESSOR_INFORMATION structure pointer, RelationCache, RelationNumaNode, RelationProcessorCore, RelationProcessorPackage, SYSTEM_LOGICAL_PROCESSOR_INFORMATION, SYSTEM_LOGICAL_PROCESSOR_INFORMATION structure, _SYSTEM_LOGICAL_PROCESSOR_INFORMATION, base.system_logical_processor_information, winnt/PSYSTEM_LOGICAL_PROCESSOR_INFORMATION, winnt/SYSTEM_LOGICAL_PROCESSOR_INFORMATION"
ms.topic: struct
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP Professional x64 Edition [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - SYSTEM_LOGICAL_PROCESSOR_INFORMATION
product: Windows
targetos: Windows
req.typenames: SYSTEM_LOGICAL_PROCESSOR_INFORMATION, *PSYSTEM_LOGICAL_PROCESSOR_INFORMATION
req.redist: 
---

# SYSTEM_LOGICAL_PROCESSOR_INFORMATION structure


## -description


Describes the relationship between the specified processor set. This structure is used with the <a href="https://msdn.microsoft.com/904d2d35-f419-4e8f-a689-f39ed926644c">GetLogicalProcessorInformation</a> function.


## -struct-fields




### -field ProcessorMask

The processor mask  identifying the processors described by this structure. A processor mask is a bit vector in which each set bit represents an active processor in the relationship. At least one bit will be set.

On a system with more than 64 processors, the processor mask identifies processors in a single <a href="https://msdn.microsoft.com/c627ac0f-96e8-48b5-9103-4316f487e173">processor group</a>.


### -field Relationship

The relationship between the processors identified by the value of the <b>ProcessorMask</b> member. This member can be one of the following <a href="https://msdn.microsoft.com/2ada52f0-70ec-4146-9ef7-9af3b08996f9">LOGICAL_PROCESSOR_RELATIONSHIP</a> values.

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

<b>Windows Server 2003:  </b>This value is not supported until Windows Server 2003 with SP1 and Windows XP Professional x64 Edition.

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
The specified logical processors share a single processor core. The <b>ProcessorCore</b> member contains additional information.

</td>
</tr>
<tr>
<td width="40%"><a id="RelationProcessorPackage"></a><a id="relationprocessorpackage"></a><a id="RELATIONPROCESSORPACKAGE"></a><dl>
<dt><b>RelationProcessorPackage</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The specified logical processors share a physical package. There is no additional information available.

<b>Windows Server 2003 and Windows XP Professional x64 Edition:  </b>This value is not supported until Windows Server 2003 with SP1 and Windows XP with SP3.

</td>
</tr>
</table>
 

Future versions of Windows may support additional values for the <b>Relationship</b> member.


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.ProcessorCore

This structure contains valid data only if the <b>Relationship</b> member is RelationProcessorCore.


### -field DUMMYUNIONNAME.ProcessorCore.Flags

 
							If the value of this member is 1, the logical processors identified by the value of the <b>ProcessorMask</b> member share functional units, as in Hyperthreading or SMT. Otherwise, the identified logical processors do not share functional units.

<b>Windows Server 2003 and Windows XP Professional x64 Edition:  </b>This member is also 1 for cores that share a physical package. Therefore, to determine whether the processor supports multiple cores or hyperthreading on systems prior to Windows Vista, use the CPUID instruction.


### -field DUMMYUNIONNAME.NumaNode

This structure contains valid data only if the <b>Relationship</b> member is RelationNumaNode.


### -field DUMMYUNIONNAME.NumaNode.NodeNumber

Identifies the <a href="https://msdn.microsoft.com/a1263968-2b26-45cc-bdd7-6aa354821a5a">NUMA</a> node. The valid values of this  parameter are 0 to the highest NUMA node number inclusive. A non-NUMA multiprocessor system will report that all processors belong to one NUMA node.


### -field DUMMYUNIONNAME.Cache

A <a href="https://msdn.microsoft.com/38cfa605-831c-45ef-a99f-55f42b2b56e9">CACHE_DESCRIPTOR</a> structure that identifies the characteristics of a particular cache. There is one record returned for each cache reported. Some or all caches may not be reported, depending on the mechanism used by the processor to identify its caches. Therefore, do not assume the absence of any particular caches. Caches are not necessarily shared among logical processors.

This structure contains valid data only if the <b>Relationship</b> member is RelationCache.

<b>Windows Server 2003:  </b>This member is not supported until Windows Server 2003 with SP1 and Windows XP Professional x64 Edition.


### -field DUMMYUNIONNAME.Reserved

Reserved. Do not use.


## -see-also




<a href="https://msdn.microsoft.com/38cfa605-831c-45ef-a99f-55f42b2b56e9">CACHE_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/904d2d35-f419-4e8f-a689-f39ed926644c">GetLogicalProcessorInformation</a>



<a href="https://msdn.microsoft.com/dfc4f444-4651-4a02-b8f6-f30d9278eae2">GetLogicalProcessorInformationEx</a>



<a href="https://msdn.microsoft.com/2ada52f0-70ec-4146-9ef7-9af3b08996f9">LOGICAL_PROCESSOR_RELATIONSHIP</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd405522(v=VS.85).aspx">SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX</a>
 

 

