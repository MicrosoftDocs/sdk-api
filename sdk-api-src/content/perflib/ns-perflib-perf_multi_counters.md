---
UID: NS:perflib._PERF_MULTI_COUNTERS
title: PERF_MULTI_COUNTERS (perflib.h)
description: Provides information about the PERF_MULTI_COUNTERS block that contains the structure.
helpviewer_keywords: ["*PPERF_MULTI_COUNTERS","PERF_MULTI_COUNTERS","PERF_MULTI_COUNTERS structure [Perf]","PPERF_MULTI_COUNTERS","PPERF_MULTI_COUNTERS structure pointer [Perf]","perf.perf_multi_counters","perflib/PERF_MULTI_COUNTERS","perflib/PPERF_MULTI_COUNTERS"]
old-location: perf\perf_multi_counters.htm
tech.root: perf
ms.assetid: 4F490C3C-F587-4E7B-B316-162EDA76EC30
ms.date: 12/05/2018
ms.keywords: '*PPERF_MULTI_COUNTERS, PERF_MULTI_COUNTERS, PERF_MULTI_COUNTERS structure [Perf], PPERF_MULTI_COUNTERS, PPERF_MULTI_COUNTERS structure pointer [Perf], perf.perf_multi_counters, perflib/PERF_MULTI_COUNTERS, perflib/PPERF_MULTI_COUNTERS'
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
req.typenames: PERF_MULTI_COUNTERS, *PPERF_MULTI_COUNTERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PERF_MULTI_COUNTERS
 - perflib/_PERF_MULTI_COUNTERS
 - PPERF_MULTI_COUNTERS
 - perflib/PPERF_MULTI_COUNTERS
 - PERF_MULTI_COUNTERS
 - perflib/PERF_MULTI_COUNTERS
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
 - PERF_MULTI_COUNTERS
---

# PERF_MULTI_COUNTERS structure


## -description

Provides information about the <b>PERF_MULTI_COUNTERS</b> block that contains the structure. A <b>PERF_MULTI_COUNTERS</b> block indicates the performance counters for which results are provided as part of the <a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_header">PERF_COUNTER_HEADER</a> block in multiple-counter query. The <b>PERF_MULTI_COUNTERS</b> block consists of a <b>PERF_MULTI_COUNTERS</b> structure
followed by a sequence of <b>DWORD</b> values that specify performance counter identifiers.

## -struct-fields

### -field dwSize

The total size of the <b>PERF_MULTI_COUNTERS</b> block, in bytes. This total size is the sum of the sizes of the <b>PERF_MULTI_COUNTERS</b> structure and all of the performance counter identifiers.

### -field dwCounters

The number of performance counter identifiers that the <b>PERF_MULTI_COUNTERS</b> block contains.

## -remarks

The <a href="/windows/desktop/api/perflib/nf-perflib-perfquerycounterdata">PerfQueryCounterData</a> function gets a <a href="/windows/desktop/api/perflib/ns-perflib-perf_data_header">PERF_DATA_HEADER</a> block that may
contain a <b>PERF_MULTI_COUNTERS</b> block within the <a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_header">PERF_COUNTER_HEADER</a> block.

## -see-also

<a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_header">PERF_COUNTER_HEADER</a>



<a href="/windows/desktop/api/perflib/ns-perflib-perf_data_header">PERF_DATA_HEADER</a>



<a href="/windows/desktop/api/perflib/nf-perflib-perfquerycounterdata">PerfQueryCounterData</a>