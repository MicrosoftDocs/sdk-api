---
UID: NS:perflib._PERF_DATA_HEADER
title: PERF_DATA_HEADER (perflib.h)
description: Provides information about the PERF_DATA_HEADER block that contains the structure.
helpviewer_keywords: ["*PPERF_DATA_HEADER","PERF_DATA_HEADER","PERF_DATA_HEADER structure [Perf]","PPERF_DATA_HEADER","PPERF_DATA_HEADER structure pointer [Perf]","perf.perf_data_header","perflib/PERF_DATA_HEADER","perflib/PPERF_DATA_HEADER"]
old-location: perf\perf_data_header.htm
tech.root: perf
ms.assetid: 0B30B30A-2B2D-43D8-B6DD-58C70D54EB58
ms.date: 12/05/2018
ms.keywords: '*PPERF_DATA_HEADER, PERF_DATA_HEADER, PERF_DATA_HEADER structure [Perf], PPERF_DATA_HEADER, PPERF_DATA_HEADER structure pointer [Perf], perf.perf_data_header, perflib/PERF_DATA_HEADER, perflib/PPERF_DATA_HEADER'
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
req.typenames: PERF_DATA_HEADER, *PPERF_DATA_HEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PERF_DATA_HEADER
 - perflib/_PERF_DATA_HEADER
 - PPERF_DATA_HEADER
 - perflib/PPERF_DATA_HEADER
 - PERF_DATA_HEADER
 - perflib/PERF_DATA_HEADER
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
 - PERF_DATA_HEADER
---

# PERF_DATA_HEADER structure


## -description

Provides information about the <b>PERF_DATA_HEADER</b> block that contains the structure. A <b>PERF_DATA_HEADER</b> block corresponds to one query specification in a query, and consists of a <b>PERF_DATA_HEADER</b> structure followed by a sequence of <a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_header">PERF_COUNTER_HEADER</a> blocks.

## -struct-fields

### -field dwTotalSize

The sum of the size of the <b>PERF_DATA_HEADER</b> structure and the sizes of all of the <a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_header">PERF_COUNTER_HEADER</a> blocks in the <b>PERF_DATA_HEADER</b> block.

### -field dwNumCounters

The number of <a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_header">PERF_COUNTER_HEADER</a> blocks that the <b>PERF_DATA_HEADER</b> block contains.

### -field PerfTimeStamp

The timestamp from a high-resolution clock.

### -field PerfTime100NSec

The number of 100 nanosecond intervals since January 1, 1601, in Coordinated Universal Time (UTC).

### -field PerfFreq

The frequency of a high-resolution clock.

### -field SystemTime

The time at which data is collected by the provider.

## -remarks

The ordering of the <a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_header">PERF_COUNTER_HEADER</a> blocks is based on the <b>Index</b> member of
the <a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_identifier">PERF_COUNTER_IDENTIFIER</a> blocks that the <a href="/windows/desktop/api/perflib/nf-perflib-perfquerycounterinfo">PerfQueryCounterInfo</a> function gets. Each
<b>PERF_COUNTER_HEADER</b> block is 8-byte aligned, so the value of the <b>dwTotalSize</b> is  a multiple
of 8 bytes.



The timestamp information in the <b>PERF_DATA_HEADER</b> structure is required when
you compute the display values of certain performance counters.

## -see-also

<a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_header">PERF_COUNTER_HEADER</a>



<a href="/windows/desktop/api/perflib/nf-perflib-perfquerycounterinfo">PerfQueryCounterInfo</a>