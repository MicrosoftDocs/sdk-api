---
UID: NS:perflib._PERF_COUNTER_DATA
title: PERF_COUNTER_DATA (perflib.h)
description: Contains information about the PERF_COUNTER_DATA block that contains the structure.
helpviewer_keywords: ["*PPERF_COUNTER_DATA","PERF_COUNTER_DATA","PERF_COUNTER_DATA structure [Perf]","PPERF_COUNTER_DATA","PPERF_COUNTER_DATA structure pointer [Perf]","perf.perf_counter_data","perflib/PERF_COUNTER_DATA","perflib/PPERF_COUNTER_DATA"]
old-location: perf\perf_counter_data.htm
tech.root: perf
ms.assetid: 19D65E98-182E-45CC-946F-F1924CB78029
ms.date: 12/05/2018
ms.keywords: '*PPERF_COUNTER_DATA, PERF_COUNTER_DATA, PERF_COUNTER_DATA structure [Perf], PPERF_COUNTER_DATA, PPERF_COUNTER_DATA structure pointer [Perf], perf.perf_counter_data, perflib/PERF_COUNTER_DATA, perflib/PPERF_COUNTER_DATA'
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
req.typenames: PERF_COUNTER_DATA, *PPERF_COUNTER_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PERF_COUNTER_DATA
 - perflib/_PERF_COUNTER_DATA
 - PPERF_COUNTER_DATA
 - perflib/PPERF_COUNTER_DATA
 - PERF_COUNTER_DATA
 - perflib/PERF_COUNTER_DATA
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
 - PERF_COUNTER_DATA
---

# PERF_COUNTER_DATA structure


## -description

Contains information about the <b>PERF_COUNTER_DATA</b> block that contains the structure. A <b>PERF_COUNTER_DATA</b> block provides raw performance counter data, and consists of the following items in order: <ol>
<li>A <b>PERF_COUNTER_DATA</b> structure.</li>
<li>Raw performance counter data.</li>
<li>Padding to make the total size of the block a multiple of eight
bytes.</li>
</ol>

## -struct-fields

### -field dwDataSize

The size of the raw performance counter data that follows the <b>PERF_COUNTER_DATA</b> structure in the <b>PERF_COUNTER_DATA</b> block, in bytes.

### -field dwSize

The total size of the <b>PERF_COUNTER_DATA</b> block, which is the sum of the sizes opf the following items:

<ul>
<li>The <b>PERF_COUNTER_DATA</b> structure</li>
<li>The raw performance counter data</li>
<li>The padding that ensures that the size of the  <b>PERF_COUNTER_DATA</b> block is a multiple of 8 bytes</li>
</ul>

## -remarks

The <a href="/windows/desktop/api/perflib/nf-perflib-perfquerycounterdata">PerfQueryCounterData</a> function returns a <a href="/windows/desktop/api/perflib/ns-perflib-perf_data_header">PERF_DATA_HEADER</a> block that may contain <b>PERF_COUNTER_DATA</b> blocks directly, or indirectly as part of a <a href="/windows/desktop/api/perflib/ns-perflib-perf_multi_instances">PERF_MULTI_INSTANCES</a> block.

## -see-also

<a href="/windows/desktop/api/perflib/nf-perflib-perfquerycounterdata">PerfQueryCounterData</a>