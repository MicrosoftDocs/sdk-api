---
UID: NS:winnt._SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX
title: "_SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX"
author: windows-driver-content
description: Contains information about the relationships of logical processors and related hardware. The GetLogicalProcessorInformationEx function uses this structure.
old-location: base\system_logical_processor_information_ex.htm
old-project: ProcThread
ms.assetid: 6ff16cda-c1dc-4d5c-ac60-756653cd6b07
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: "*PSYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX, PSYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX, PSYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX structure pointer, RelationCache, RelationGroup, RelationNumaNode, RelationProcessorCore, RelationProcessorPackage, SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX, SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX structure, _SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX, base.system_logical_processor_information_ex, winnt/PSYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX, winnt/SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX, *PSYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinNT.h
api_name:
-	SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX structure


## -description


Contains information about the relationships of logical processors and related hardware. The <a href="https://msdn.microsoft.com/dfc4f444-4651-4a02-b8f6-f30d9278eae2">GetLogicalProcessorInformationEx</a> function uses this structure.


## -struct-fields




### -field DUMMYUNIONNAME

 


### -field Relationship

The type of relationship between the logical processors. This parameter can be one of the following <a href="https://msdn.microsoft.com/2ada52f0-70ec-4146-9ef7-9af3b08996f9">LOGICAL_PROCESSOR_RELATIONSHIP</a> values.

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


#### - Cache

A <a href="https://msdn.microsoft.com/f8fe521b-02d6-4c58-8ef8-653280add111">CACHE_RELATIONSHIP</a> structure that describes cache attributes. This structure contains valid data only if the <b>Relationship</b> member is <b>RelationCache</b>.


#### - Group

A <a href="https://msdn.microsoft.com/3529ddef-04c5-4573-877d-c225da684e38">GROUP_RELATIONSHIP</a> structure that contains information about the processor groups. This structure contains valid data only if the <b>Relationship</b> member is <b>RelationGroup</b>.


#### - NumaNode

A <a href="https://msdn.microsoft.com/a4e4c994-c4af-4b4f-8684-6037bcba35a9">NUMA_NODE_RELATIONSHIP</a> structure that describes a NUMA node. This structure contains valid data only if the <b>Relationship</b> member is <b>RelationNumaNode</b>.


#### - Processor

A <a href="https://msdn.microsoft.com/1efda80d-cf5b-4312-801a-ea3585b152ac">PROCESSOR_RELATIONSHIP</a> structure that describes processor affinity. This structure contains valid data only if the <b>Relationship</b> member is <b>RelationProcessorCore</b> or <b>RelationProcessorPackage</b>.


## -see-also




<a href="https://msdn.microsoft.com/f8fe521b-02d6-4c58-8ef8-653280add111">CACHE_RELATIONSHIP</a>



<a href="https://msdn.microsoft.com/3529ddef-04c5-4573-877d-c225da684e38">GROUP_RELATIONSHIP</a>



<a href="https://msdn.microsoft.com/a4e4c994-c4af-4b4f-8684-6037bcba35a9">NUMA_NODE_RELATIONSHIP</a>



<a href="https://msdn.microsoft.com/1efda80d-cf5b-4312-801a-ea3585b152ac">PROCESSOR_RELATIONSHIP</a>
 

 

