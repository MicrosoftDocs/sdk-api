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

# _SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX structure


## -description


Contains information about the relationships of logical processors and related hardware. The <a href="https://msdn.microsoft.com/dfc4f444-4651-4a02-b8f6-f30d9278eae2">GetLogicalProcessorInformationEx</a> function uses this structure.


## -struct-fields




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


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.Processor

A <a href="https://msdn.microsoft.com/1efda80d-cf5b-4312-801a-ea3585b152ac">PROCESSOR_RELATIONSHIP</a> structure that describes processor affinity. This structure contains valid data only if the <b>Relationship</b> member is <b>RelationProcessorCore</b> or <b>RelationProcessorPackage</b>.


### -field DUMMYUNIONNAME.NumaNode

A <a href="https://msdn.microsoft.com/a4e4c994-c4af-4b4f-8684-6037bcba35a9">NUMA_NODE_RELATIONSHIP</a> structure that describes a NUMA node. This structure contains valid data only if the <b>Relationship</b> member is <b>RelationNumaNode</b>.


### -field DUMMYUNIONNAME.Cache

A <a href="https://msdn.microsoft.com/f8fe521b-02d6-4c58-8ef8-653280add111">CACHE_RELATIONSHIP</a> structure that describes cache attributes. This structure contains valid data only if the <b>Relationship</b> member is <b>RelationCache</b>.


### -field DUMMYUNIONNAME.Group

A <a href="https://msdn.microsoft.com/3529ddef-04c5-4573-877d-c225da684e38">GROUP_RELATIONSHIP</a> structure that contains information about the processor groups. This structure contains valid data only if the <b>Relationship</b> member is <b>RelationGroup</b>.


## -see-also




<a href="https://msdn.microsoft.com/f8fe521b-02d6-4c58-8ef8-653280add111">CACHE_RELATIONSHIP</a>



<a href="https://msdn.microsoft.com/3529ddef-04c5-4573-877d-c225da684e38">GROUP_RELATIONSHIP</a>



<a href="https://msdn.microsoft.com/a4e4c994-c4af-4b4f-8684-6037bcba35a9">NUMA_NODE_RELATIONSHIP</a>



<a href="https://msdn.microsoft.com/1efda80d-cf5b-4312-801a-ea3585b152ac">PROCESSOR_RELATIONSHIP</a>
 

 

