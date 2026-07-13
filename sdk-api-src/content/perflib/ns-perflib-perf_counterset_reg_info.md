---
UID: NS:perflib._PERF_COUNTERSET_REG_INFO
title: PERF_COUNTERSET_REG_INFO (perflib.h)
description: Contains information about the PERF_COUNTERSET_REG_INFO block that contains the structure.
helpviewer_keywords: ["*PPERF_COUNTERSET_REG_INFO","PERF_COUNTERSET_INSTANCE_AGGREGATE","PERF_COUNTERSET_MULTI_AGGREGATE","PERF_COUNTERSET_MULTI_INSTANCES","PERF_COUNTERSET_REG_INFO","PERF_COUNTERSET_REG_INFO structure [Perf]","PERF_COUNTERSET_SINGLE_AGGREGATE","PERF_COUNTERSET_SINGLE_AGGREGATE_HISTORY","PERF_COUNTERSET_SINGLE_INSTANCE","PERF_DETAIL_ADVANCED","PERF_DETAIL_NOVICE","PPERF_COUNTERSET_REG_INFO","PPERF_COUNTERSET_REG_INFO structure pointer [Perf]","perf.perf_counterset_reg_info","perflib/PERF_COUNTERSET_REG_INFO","perflib/PPERF_COUNTERSET_REG_INFO"]
old-location: perf\perf_counterset_reg_info.htm
tech.root: perf
ms.assetid: D220426F-7849-47DF-A411-5381FC39CA80
ms.date: 12/05/2018
ms.keywords: '*PPERF_COUNTERSET_REG_INFO, PERF_COUNTERSET_INSTANCE_AGGREGATE, PERF_COUNTERSET_MULTI_AGGREGATE, PERF_COUNTERSET_MULTI_INSTANCES, PERF_COUNTERSET_REG_INFO, PERF_COUNTERSET_REG_INFO structure [Perf], PERF_COUNTERSET_SINGLE_AGGREGATE, PERF_COUNTERSET_SINGLE_AGGREGATE_HISTORY, PERF_COUNTERSET_SINGLE_INSTANCE, PERF_DETAIL_ADVANCED, PERF_DETAIL_NOVICE, PPERF_COUNTERSET_REG_INFO, PPERF_COUNTERSET_REG_INFO structure pointer [Perf], perf.perf_counterset_reg_info, perflib/PERF_COUNTERSET_REG_INFO, perflib/PPERF_COUNTERSET_REG_INFO'
req.header: perflib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: PERF_COUNTERSET_REG_INFO, *PPERF_COUNTERSET_REG_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PERF_COUNTERSET_REG_INFO
 - perflib/_PERF_COUNTERSET_REG_INFO
 - PPERF_COUNTERSET_REG_INFO
 - perflib/PPERF_COUNTERSET_REG_INFO
 - PERF_COUNTERSET_REG_INFO
 - perflib/PERF_COUNTERSET_REG_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Perflib.h
api_name:
 - PERF_COUNTERSET_REG_INFO
---

# PERF_COUNTERSET_REG_INFO structure


## -description

Contains information about the <b>PERF_COUNTERSET_REG_INFO</b> block that contains the structure. A <b>PERF_COUNTERSET_REG_INFO</b> block provides registration information for a counter set and the performance counters it contains, and consists of a <b>PERF_COUNTERSET_REG_INFO</b> structure immediately followed by a set
<a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_reg_info">PERF_COUNTER_REG_INFO</a> structures that correspond to the performance counters in the counter set.

## -struct-fields

### -field CounterSetGuid

The unique identifier for the counter set.

### -field CounterSetType

Reserved.

### -field DetailLevel

The target audience for the counters in the counter set. 


The possible values are:



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PERF_DETAIL_NOVICE"></a><a id="perf_detail_novice"></a><dl>
<dt><b>PERF_DETAIL_NOVICE</b></dt>
</dl>
</td>
<td width="60%">
You can display the counter to any level of user.

</td>
</tr>
<tr>
<td width="40%"><a id="PERF_DETAIL_ADVANCED"></a><a id="perf_detail_advanced"></a><dl>
<dt><b>PERF_DETAIL_ADVANCED</b></dt>
</dl>
</td>
<td width="60%">
The counter is complicated and should be displayed only to advanced users.

</td>
</tr>
</table>

### -field NumCounters

The number of <a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_reg_info">PERF_COUNTER_REG_INFO</a> structures in this  <b>PERF_COUNTERSET_REG_INFO</b> block.

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
Not implemented.

</td>
</tr>
</table>

## -remarks

The <a href="/windows/desktop/api/perflib/nf-perflib-perfquerycountersetregistrationinfo">PerfQueryCounterSetRegistrationInfo</a> function called with the <i>requestCode</i> parameter set to
<b>PERF_REG_COUNTERSET_STRUCT</b> gets a <b>PERF_COUNTERSET_REG_INFO</b> block.