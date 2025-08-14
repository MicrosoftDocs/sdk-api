---
UID: NF:perflib.PerfAddCounters
title: PerfAddCounters function (perflib.h)
description: Adds performance counter specifications to the specified query.
helpviewer_keywords: ["PerfAddCounters","PerfAddCounters function [Perf]","perf.perfaddcounters","perflib/PerfAddCounters"]
old-location: perf\perfaddcounters.htm
tech.root: perf
ms.assetid: FC66E794-EF13-47BB-A704-735924363310
ms.date: 12/05/2018
ms.keywords: PerfAddCounters, PerfAddCounters function [Perf], perf.perfaddcounters, perflib/PerfAddCounters
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
req.lib: AdvAPI32.lib
req.dll: AdvAPI32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PerfAddCounters
 - perflib/PerfAddCounters
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-perf-legacy-l1-1-0.dll
 - AdvAPI32.dll
api_name:
 - PerfAddCounters
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
<a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -remarks

The <i>pCounters</i> parameter should point to a sequence of <a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_identifier">PERF_COUNTER_IDENTIFIER</a> blocks. Each <b>PERF_COUNTER_IDENTIFIER</b> block consists of a
<b>PERF_COUNTER_IDENTIFIER</b> structure, optionally followed by a null-terminated
UTF-16LE instance  name string, followed by padding that makes the size of the block a multiple of 8 bytes.

For each <a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_identifier">PERF_COUNTER_IDENTIFIER</a> block:

<ul>
<li>Set the <b>CounterSetGuid</b> member of the <a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_identifier">PERF_COUNTER_IDENTIFIER</a> structure to the identifier of the counter set to be queried.
</li>
<li>Set the <b>Status</b> member of the <a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_identifier">PERF_COUNTER_IDENTIFIER</a> structure to 0.</li>
<li>Set <b>Size</b> member of the <a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_identifier">PERF_COUNTER_IDENTIFIER</a> structure to the size of the <b>PERF_COUNTER_IDENTIFIER</b> block in bytes, including the
  <b>PERF_COUNTER_IDENTIFIER</b> structure, the instance name, and the padding. The
  value of <b>Size</b> must be a multiple of 8.</li>
<li>Set the <b>CounterId</b> member of the <a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_identifier">PERF_COUNTER_IDENTIFIER</a> structure to the identifier of the counter that should be returned by the query.
  To return all counters, set <b>CounterId</b> to <b>PERF_WILDCARD_COUNTER</b>.</li>
<li>Set the <b>InstanceId</b> member of the <a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_identifier">PERF_COUNTER_IDENTIFIER</a> structure to the identifier of the instance that should be returned by the
  query. If no filtering should be done based on instance identifier, set
  <b>InstanceId</b> to <b>PERF_WILDCARD_COUNTER</b>.</li>
<li>Set the <b>Index</b> member of the <a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_identifier">PERF_COUNTER_IDENTIFIER</a> structure to 0.</li>
<li>Set the <b>Reserved</b> member of the <a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_identifier">PERF_COUNTER_IDENTIFIER</a> structure to 0.
</li>
<li>Include the instance name immediately after the <a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_identifier">PERF_COUNTER_IDENTIFIER</a> structure. <ul>
<li>If the counter set is single-instance, do not set the instance name. In this case, the value of the Size member of the <a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_identifier">PERF_COUNTER_IDENTIFIER</a> structure must be  the size of the <b>PERF_COUNTER_IDENTIFIER</b> structure. </li>
<li>If the
  counter set is multiple-instance, you must set the instance name. If you do not want to filter the performance counter specifications based on instance name, use <b>PERF_WILDCARD_INSTANCE</b> as the
  instance name.

</li>
</ul>
</li>
</ul>
<b>PerfAddCounters</b> attempts to add one counter specification to the query for
each <a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_identifier">PERF_COUNTER_IDENTIFIER</a> block, and updates the <b>Status</b> member of the <b>PERF_COUNTER_IDENTIFIER</b> structure in each
block with the result of the attempt.

## -see-also

<a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_identifier">PERF_COUNTER_IDENTIFIER</a>



<a href="/windows/desktop/api/perflib/nf-perflib-perfdeletecounters">PerfDeleteCounters</a>