---
UID: NS:perflib._PERF_MULTI_INSTANCES
title: PERF_MULTI_INSTANCES (perflib.h)
description: Provides information about the PERF_MULTI_INSTANCES block that contains the structure.
helpviewer_keywords: ["*PPERF_MULTI_INSTANCES","PERF_MULTI_INSTANCES","PERF_MULTI_INSTANCES structure [Perf]","PPERF_MULTI_INSTANCES","PPERF_MULTI_INSTANCES structure pointer [Perf]","perf.perf_multi_instances","perflib/PERF_MULTI_INSTANCES","perflib/PPERF_MULTI_INSTANCES"]
old-location: perf\perf_multi_instances.htm
tech.root: perf
ms.assetid: 5EC34ECD-D240-4B44-A52B-C5518918400C
ms.date: 12/05/2018
ms.keywords: '*PPERF_MULTI_INSTANCES, PERF_MULTI_INSTANCES, PERF_MULTI_INSTANCES structure [Perf], PPERF_MULTI_INSTANCES, PPERF_MULTI_INSTANCES structure pointer [Perf], perf.perf_multi_instances, perflib/PERF_MULTI_INSTANCES, perflib/PPERF_MULTI_INSTANCES'
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
req.typenames: PERF_MULTI_INSTANCES, *PPERF_MULTI_INSTANCES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PERF_MULTI_INSTANCES
 - perflib/_PERF_MULTI_INSTANCES
 - PPERF_MULTI_INSTANCES
 - perflib/PPERF_MULTI_INSTANCES
 - PERF_MULTI_INSTANCES
 - perflib/PERF_MULTI_INSTANCES
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
 - PERF_MULTI_INSTANCES
---

# PERF_MULTI_INSTANCES structure


## -description

Provides information about the <b>PERF_MULTI_INSTANCES</b> block that contains the structure. A <b>PERF_MULTI_INSTANCES</b> block indicates the number of instances for which results are provided as part of the <a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_header">PERF_COUNTER_HEADER</a> block in multiple-instance query. The <b>PERF_MULTI_INSTANCES</b> block consists of the following items in order:<ol>
<li>A <b>PERF_MULTI_INSTANCES</b> structure</li>
<li>A number of instance data blocks. The number of instance data blocks that the <b>PERF_MULTI_INSTANCES</b> block contains is indicated ny the <b>dwInstances</b> member of the <b>PERF_MULTI_INSTANCES</b> structure. Each instance data block
consists of the following items in order:<ol>
<li>A <a href="/windows/desktop/api/perflib/ns-perflib-perf_instance_header">PERF_INSTANCE_HEADER</a> block</li>
<li>A number of
<a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_data">PERF_COUNTER_DATA</a> blocks. The number of <b>PERF_COUNTER_DATA</b> blocks depends on
the context:<ul>
<li>If the <b>PERF_MULTI_INSTANCES</b> block is part of a
<a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_header">PERF_COUNTER_HEADER</a> block with type <b>PERF_MULTIPLE_INSTANCES</b>, the instance data block contains one
<a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_data">PERF_COUNTER_DATA</a> block.</li>
<li> If the <b>PERF_MULTI_INSTANCES</b> block is part of a
<a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_header">PERF_COUNTER_HEADER</a> block with type <b>PERF_COUNTERSET</b>, the number of
<a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_data">PERF_COUNTER_DATA</a> blocks is indicated by the <a href="/windows/desktop/api/perflib/ns-perflib-perf_multi_counters">PERF_MULTI_COUNTERS</a> block.</li>
</ul>
</li>
</ol>
</li>
</ol>

## -struct-fields

### -field dwTotalSize

The total size of the <b>PERF_MULTI_INSTANCES</b> block, in bytes. This total size is the sum of the sizes of the <b>PERF_MULTI_INSTANCES</b> structure and the instance data blocks.

### -field dwInstances

The number of instance data blocks in the <b>PERF_MULTI_INSTANCES</b> block.

## -remarks

The <a href="/windows/desktop/api/perflib/nf-perflib-perfquerycounterdata">PerfQueryCounterData</a> function gets a <a href="/windows/desktop/api/perflib/ns-perflib-perf_data_header">PERF_DATA_HEADER</a> block that may
contain <b>PERF_MULTI_INSTANCES</b> blocks within the <a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_header">PERF_COUNTER_HEADER</a> block.

## -see-also

<a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_header">PERF_COUNTER_HEADER</a>



<a href="/windows/desktop/api/perflib/ns-perflib-perf_data_header">PERF_DATA_HEADER</a>



<a href="/windows/desktop/api/perflib/nf-perflib-perfquerycounterdata">PerfQueryCounterData</a>