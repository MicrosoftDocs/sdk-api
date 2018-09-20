---
UID: NS:perflib._PERF_COUNTERSET_INFO
title: "_PERF_COUNTERSET_INFO"
author: windows-sdk-content
description: Defines information about a counter set that a provider uses. The CTRPP tool automatically generates this structure based on the schema you specify.
old-location: perf\perf_counterset_info.htm
tech.root: perfctrs
ms.assetid: bf48dcdb-6fdd-4093-9006-a53690c3ed86
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: "*PPERF_COUNTERSET_INFO, PERF_COUNTERSET_INFO, PERF_COUNTERSET_INFO structure [Perf], PERF_COUNTERSET_INFO,*PPERF_COUNTERSET_INFO, PERF_COUNTERSET_INFO,*PPERF_COUNTERSET_INFO structure [Perf], PERF_COUNTERSET_INSTANCE_AGGREGATE, PERF_COUNTERSET_MULTI_AGGREGATE, PERF_COUNTERSET_MULTI_INSTANCES, PERF_COUNTERSET_SINGLE_AGGREGATE, PERF_COUNTERSET_SINGLE_AGGREGATE_HISTORY, PERF_COUNTERSET_SINGLE_INSTANCE, _PERF_COUNTERSET_INFO, base.perf_counterset_info, perf.perf_counterset_info, perflib/PERF_COUNTERSET_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: perflib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - Perflib.h
api_name:
 - PERF_COUNTERSET_INFO, *PPERF_COUNTERSET_INFO
product: Windows
targetos: Windows
req.typenames: PERF_COUNTERSET_INFO, *PPERF_COUNTERSET_INFO
req.redist: 
---

# _PERF_COUNTERSET_INFO structure


## -description


Defines information about a counter set that a provider uses.  The <a href="https://msdn.microsoft.com/3939f6a1-0a94-429d-a71e-b37f045fea13">CTRPP</a> tool automatically generates this structure based on the  schema you specify.


## -struct-fields




### -field CounterSetGuid

GUID that uniquely identifies the counter set. The <b>guid</b> attribute of the <a href="perf.counterset_element">counterSet</a> element contains the GUID.


### -field ProviderGuid

GUID that uniquely identifies the provider that supports the counter set. The <b>providerGuid</b> attribute of the <a href="https://msdn.microsoft.com/10112f43-f483-4ecb-aa7d-60efaad149c6">provider</a> element contains the GUID.


### -field NumCounters

Number of counters in the counter set. See Remarks.


### -field InstanceType

Specifies whether the counter set allows multiple instances such as processes and physical disks, or    a single instance such as memory. 


The following are the possible instance types.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PERF_COUNTERSET_SINGLE_INSTANCE"></a><a id="perf_counterset_single_instance"></a><dl>
<dt><b>PERF_COUNTERSET_SINGLE_INSTANCE</b></dt>
</dl>
</td>
<td width="60%">
The counter set contains single instance counters, for example, a counter that measures physical memory.

</td>
</tr>
<tr>
<td width="40%"><a id="PERF_COUNTERSET_MULTI_INSTANCES"></a><a id="perf_counterset_multi_instances"></a><dl>
<dt><b>PERF_COUNTERSET_MULTI_INSTANCES</b></dt>
</dl>
</td>
<td width="60%">
The counter set contains multiple instance counters, for example, a counter that measures the average disk I/O for a process.

</td>
</tr>
<tr>
<td width="40%"><a id="PERF_COUNTERSET_SINGLE_AGGREGATE"></a><a id="perf_counterset_single_aggregate"></a><dl>
<dt><b>PERF_COUNTERSET_SINGLE_AGGREGATE</b></dt>
</dl>
</td>
<td width="60%">
The counter set contains single instance counters whose aggregate value is obtained from one or more sources. For example, a counter in this type of counter set might obtain the number of reads from each of the three hard disks on the computer and sum their values. 

</td>
</tr>
<tr>
<td width="40%"><a id="PERF_COUNTERSET_MULTI_AGGREGATE"></a><a id="perf_counterset_multi_aggregate"></a><dl>
<dt><b>PERF_COUNTERSET_MULTI_AGGREGATE</b></dt>
</dl>
</td>
<td width="60%">
The counter set contains multiple instance counters whose aggregate value is obtained from all instances of the counter. For example, a counter in this type of counter set might obtain the total thread execution time for all threads in a multi-threaded application and sum their values.

</td>
</tr>
<tr>
<td width="40%"><a id="PERF_COUNTERSET_SINGLE_AGGREGATE_HISTORY"></a><a id="perf_counterset_single_aggregate_history"></a><dl>
<dt><b>PERF_COUNTERSET_SINGLE_AGGREGATE_HISTORY</b></dt>
</dl>
</td>
<td width="60%">
The difference between this type and <b>PERF_COUNTERSET_SINGLE_AGGREGATE</b> is that this counter set type stores all counter values for the lifetime of the consumer application (the counter value is cached beyond the lifetime of the counter). For example, if one of the hard disks in the single aggregate example above were to become unavailable, the total bytes read by that disk would still be available and used to calculate the aggregate value. 

</td>
</tr>
<tr>
<td width="40%"><a id="PERF_COUNTERSET_INSTANCE_AGGREGATE"></a><a id="perf_counterset_instance_aggregate"></a><dl>
<dt><b>PERF_COUNTERSET_INSTANCE_AGGREGATE</b></dt>
</dl>
</td>
<td width="60%">
This type is similar to PERF_COUNTERSET_MULTI_AGGREGATE, except that instead of aggregating all instance data to one aggregated (_Total) instance, it will aggregate counter data from instances of the same name.

 

For example, if multiple provider processes contained instances named IExplore, PERF_COUNTERSET_MULTIPLE and PERF_COUNTERSET_MULTI_AGGREGATE CounterSet will show multiple IExplore instances (IExplore, IExplore#1, IExplore#2, and so on); however, a PERF_COUNTERSET_INSTANCE_AGGREGATE instance type will only publish one IExplore instance with aggregated counter data from all instances named IExplore.


<b>Windows Vista:  </b>This type is not available.



</td>
</tr>
</table>
 


## -remarks



The memory block for this structure also contains one or more <a href="https://msdn.microsoft.com/f1fb6ad5-ad38-46d0-b76d-803887ba3d97">PERF_COUNTER_INFO</a> structures. The <b>NumCounter</b> member determines the number of <b>PERF_COUNTER_INFO</b> structures that follow this structure in memory.




## -see-also




<a href="https://msdn.microsoft.com/f1fb6ad5-ad38-46d0-b76d-803887ba3d97">PERF_COUNTER_INFO</a>



<a href="https://msdn.microsoft.com/b4295503-5588-4898-816c-939a5920fc77">PerfSetCounterSetInfo</a>
 

 

