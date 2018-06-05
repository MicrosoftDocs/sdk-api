---
UID: NS:perflib._PERF_COUNTER_IDENTIFIER
title: "_PERF_COUNTER_IDENTIFIER"
author: windows-sdk-content
description: Contains information about the PERF_COUNTER_IDENTIFIER block that contains the structure.
old-location: perf\perf_counter_identifier.htm
old-project: PerfCtrs
ms.assetid: 4BBAB831-9A7F-407E-A7D6-9123192C12B4
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: "*PPERF_COUNTER_IDENTIFIER, PERF_COUNTER_IDENTIFIER, PERF_COUNTER_IDENTIFIER structure [Perf], PPERF_COUNTER_IDENTIFIER, PPERF_COUNTER_IDENTIFIER structure pointer [Perf], _PERF_COUNTER_IDENTIFIER, perf.perf_counter_identifier, perflib/PERF_COUNTER_IDENTIFIER, perflib/PPERF_COUNTER_IDENTIFIER"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: PERF_COUNTER_IDENTIFIER, *PPERF_COUNTER_IDENTIFIER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Perflib.h
api_name:
-	PERF_COUNTER_IDENTIFIER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _PERF_COUNTER_IDENTIFIER structure


## -description


Contains information about the <b>PERF_COUNTER_IDENTIFIER</b> block that contains the structure. A <b>PERF_COUNTER_IDENTIFIER</b> block provides information about a performance counter specification, and consists of the following items in order: <ol>
<li>A <b>PERF_COUNTER_IDENTIFIER</b>
structure</li>
<li>An optional null-terminated UTF-16LE string that specifies the instance name</li>
<li>
Padding as needed to make the size of the block  a multiple of 8 bytes. </li>
</ol>



## -struct-fields




### -field CounterSetGuid

The <b>GUID</b> of the performance counter set.


### -field Status

An error code  that indicates whether the operation to add or delete a performance counter succeeded or failed.


### -field Size

The total size of the <b>PERF_COUNTER_IDENTIFIER</b> block, in bytes. The total size of the block is the sum of the sizes of the <b>PERF_COUNTER_IDENTIFIER</b> structure, the string that specifies the instance name, and the padding.


### -field CounterId

The identifier of the performance counter. <b>PERF_WILDCARD_COUNTER</b> specifies  all counters.


### -field InstanceId

The instance identifier. Specify 0xFFFFFFFF if you do  not want to filter the results based on the instance identifier.


### -field Index

The position in the sequence of <b>PERF_COUNTER_IDENTIFIER</b> blocks at which the counter data that corresponds to this <b>PERF_COUNTER_IDENTIFIER</b> block is returned. Set by <a href="https://msdn.microsoft.com/42CAB98C-4525-499D-BA11-731A666E112D">PerfQueryCounterInfo</a>.


### -field Reserved

Reserved.


## -remarks



When you specify a counter set identifier for a single-instance counter set, you must not specify the
instance name in the additional data of the <b>PERF_COUNTER_IDENTIFIER</b> block. The size of the <b>PERF_COUNTER_IDENTIFIER</b> block must be the size of the <b>PERF_COUNTER_IDENTIFIER</b> structure.

On the other hand, when you specify a counter set identifier for a multiple-instance counter set, you must specify the instance name in the additional data of the <b>PERF_COUNTER_IDENTIFIER</b> block. The identifier is notconsidered valid unless the size of
the <b>PERF_COUNTER_IDENTIFIER</b> block is greater than the  size of the <b>PERF_COUNTER_IDENTIFIER</b> structure. If you do not want
to filter the counter sets based on the instance name, use <b>PERF_WILDCARD_INSTANCE</b> as the instance
name.

The <a href="https://msdn.microsoft.com/FC66E794-EF13-47BB-A704-735924363310">PerfAddCounters</a> and <a href="https://msdn.microsoft.com/330CA041-41CA-4C48-B88B-C48A0143505E">PerfDeleteCounters</a> functions accept a sequence of
<b>PERF_COUNTER_IDENTIFIER</b> blocks to define the counter specifications that you want to be
add or remove from a query.

The <a href="https://msdn.microsoft.com/42CAB98C-4525-499D-BA11-731A666E112D">PerfQueryCounterInfo</a> function gets a sequence of <b>PERF_COUNTER_IDENTIFIER</b>
blocks to indicate the counter specifications in a query and to indicate in the <b>Index</b> member the
order in which the  query gets the results.




## -see-also




<a href="https://msdn.microsoft.com/FC66E794-EF13-47BB-A704-735924363310">PerfAddCounters</a>



<a href="https://msdn.microsoft.com/330CA041-41CA-4C48-B88B-C48A0143505E">PerfDeleteCounters</a>



<a href="https://msdn.microsoft.com/42CAB98C-4525-499D-BA11-731A666E112D">PerfQueryCounterInfo</a>
 

 

