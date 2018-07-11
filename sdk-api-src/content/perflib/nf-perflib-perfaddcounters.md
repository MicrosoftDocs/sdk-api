---
UID: NF:perflib.PerfAddCounters
title: PerfAddCounters function
author: windows-sdk-content
description: Adds performance counter specifications to the specified query.
old-location: perf\perfaddcounters.htm
old-project: perfctrs
ms.assetid: FC66E794-EF13-47BB-A704-735924363310
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: PerfAddCounters, PerfAddCounters function [Perf], perf.perfaddcounters, perflib/PerfAddCounters
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: PerfRegInfoType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - AdvAPI32.dll
api_name:
 - PerfAddCounters
product: Windows
targetos: Windows
req.lib: AdvAPI32.lib
req.dll: AdvAPI32.dll
req.irql: 
req.product: ADAM
---

# PerfAddCounters function


## -description


Adds performance counter specifications to the specified query.



## -parameters




### -param hQuery [in]

A handle to the query to which you want to add performance counter specifications.


### -param pCounters [in, out]

A pointer to the performance counter specifications that you want to add.


### -param cbCounters

The size of the buffer that the <i>pCounters</i> parameter specifies, in bytes.


## -returns




						If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. 




## -remarks



The <i>pCounters</i> parameter should point to a sequence of <a href="https://msdn.microsoft.com/4BBAB831-9A7F-407E-A7D6-9123192C12B4">PERF_COUNTER_IDENTIFIER</a>
blocks. Each <b>PERF_COUNTER_IDENTIFIER</b> block consists of a
<b>PERF_COUNTER_IDENTIFIER</b> structure, optionally followed by a null-terminated
UTF-16LE instance  name string, followed by padding that makes the size of the block a multiple of 8 bytes.

For each <a href="https://msdn.microsoft.com/4BBAB831-9A7F-407E-A7D6-9123192C12B4">PERF_COUNTER_IDENTIFIER</a> block:

<ul>
<li>Set the <b>CounterSetGuid</b> member of the <a href="https://msdn.microsoft.com/4BBAB831-9A7F-407E-A7D6-9123192C12B4">PERF_COUNTER_IDENTIFIER</a> structure to the identifier of the counter set to be queried.
</li>
<li>Set the <b>Status</b> member of the <a href="https://msdn.microsoft.com/4BBAB831-9A7F-407E-A7D6-9123192C12B4">PERF_COUNTER_IDENTIFIER</a> structure to 0.</li>
<li>Set <b>Size</b> member of the <a href="https://msdn.microsoft.com/4BBAB831-9A7F-407E-A7D6-9123192C12B4">PERF_COUNTER_IDENTIFIER</a> structure to the size of the <b>PERF_COUNTER_IDENTIFIER</b> block in bytes, including the
  <b>PERF_COUNTER_IDENTIFIER</b> structure, the instance name, and the padding. The
  value of <b>Size</b> must be a multiple of 8.</li>
<li>Set the <b>CounterId</b> member of the <a href="https://msdn.microsoft.com/4BBAB831-9A7F-407E-A7D6-9123192C12B4">PERF_COUNTER_IDENTIFIER</a> structure to the identifier of the counter that should be returned by the query.
  To return all counters, set <b>CounterId</b> to <b>PERF_WILDCARD_COUNTER</b>.</li>
<li>Set the <b>InstanceId</b> member of the <a href="https://msdn.microsoft.com/4BBAB831-9A7F-407E-A7D6-9123192C12B4">PERF_COUNTER_IDENTIFIER</a> structure to the identifier of the instance that should be returned by the
  query. If no filtering should be done based on instance identifier, set
  <b>InstanceId</b> to <b>PERF_WILDCARD_COUNTER</b>.</li>
<li>Set the <b>Index</b> member of the <a href="https://msdn.microsoft.com/4BBAB831-9A7F-407E-A7D6-9123192C12B4">PERF_COUNTER_IDENTIFIER</a> structure to 0.</li>
<li>Set the <b>Reserved</b> member of the <a href="https://msdn.microsoft.com/4BBAB831-9A7F-407E-A7D6-9123192C12B4">PERF_COUNTER_IDENTIFIER</a> structure to 0.
</li>
<li>Include the instance name immediately after the <a href="https://msdn.microsoft.com/4BBAB831-9A7F-407E-A7D6-9123192C12B4">PERF_COUNTER_IDENTIFIER</a>
  structure. <ul>
<li>If the counter set is single-instance, do not set the instance name. In this case, the value of the Size member of the <a href="https://msdn.microsoft.com/4BBAB831-9A7F-407E-A7D6-9123192C12B4">PERF_COUNTER_IDENTIFIER</a> structure must be  the size of the <b>PERF_COUNTER_IDENTIFIER</b> structure. </li>
<li>If the
  counter set is multiple-instance, you must set the instance name. If you do not want to filter the performance counter specifications based on instance name, use <b>PERF_WILDCARD_INSTANCE</b> as the
  instance name.

</li>
</ul>
</li>
</ul>
<b>PerfAddCounters</b> attempts to add one counter specification to the query for
each <a href="https://msdn.microsoft.com/4BBAB831-9A7F-407E-A7D6-9123192C12B4">PERF_COUNTER_IDENTIFIER</a> block, and updates the <b>Status</b> member of the <b>PERF_COUNTER_IDENTIFIER</b> structure in each
block with the result of the attempt. 




## -see-also




<a href="https://msdn.microsoft.com/4BBAB831-9A7F-407E-A7D6-9123192C12B4">PERF_COUNTER_IDENTIFIER</a>



<a href="https://msdn.microsoft.com/330CA041-41CA-4C48-B88B-C48A0143505E">PerfDeleteCounters</a>
 

 

