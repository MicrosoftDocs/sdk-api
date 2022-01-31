---
UID: NE:perflib._PerfCounterDataType
title: PerfCounterDataType (perflib.h)
description: Indicates the content type of a PERF_COUNTER_HEADER block that the PerfQueryCounterData function includes as part of the PERF_DATA_HEADER block that the function produces as output.
helpviewer_keywords: ["PERF_COUNTERSET","PERF_ERROR_RETURN","PERF_MULTIPLE_COUNTERS","PERF_MULTIPLE_INSTANCES","PERF_SINGLE_COUNTER","PerfCounterDataType","PerfCounterDataType enumeration [Perf]","perf.perfcounterdatatype","perflib/PERF_COUNTERSET","perflib/PERF_ERROR_RETURN","perflib/PERF_MULTIPLE_COUNTERS","perflib/PERF_MULTIPLE_INSTANCES","perflib/PERF_SINGLE_COUNTER","perflib/PerfCounterDataType"]
old-location: perf\perfcounterdatatype.htm
tech.root: perf
ms.assetid: E64C73F0-034E-408B-8537-CE6855C01347
ms.date: 12/05/2018
ms.keywords: PERF_COUNTERSET, PERF_ERROR_RETURN, PERF_MULTIPLE_COUNTERS, PERF_MULTIPLE_INSTANCES, PERF_SINGLE_COUNTER, PerfCounterDataType, PerfCounterDataType enumeration [Perf], perf.perfcounterdatatype, perflib/PERF_COUNTERSET, perflib/PERF_ERROR_RETURN, perflib/PERF_MULTIPLE_COUNTERS, perflib/PERF_MULTIPLE_INSTANCES, perflib/PERF_SINGLE_COUNTER, perflib/PerfCounterDataType
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
req.typenames: PerfCounterDataType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PerfCounterDataType
 - perflib/_PerfCounterDataType
 - PerfCounterDataType
 - perflib/PerfCounterDataType
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
 - PerfCounterDataType
---

# PerfCounterDataType enumeration


## -description

Indicates the content type of a <a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_header">PERF_COUNTER_HEADER</a> block that the <a href="/windows/desktop/api/perflib/nf-perflib-perfquerycounterdata">PerfQueryCounterData</a> function includes as part of the <a href="/windows/desktop/api/perflib/ns-perflib-perf_data_header">PERF_DATA_HEADER</a> block that the function produces as output.

## -enum-fields

### -field PERF_ERROR_RETURN:0

An error occurred when the performance counter value was queried.

### -field PERF_SINGLE_COUNTER:1

The query returned a single counter from a single instance.

### -field PERF_MULTIPLE_COUNTERS:2

The query returned multiple counters from a single instance.

### -field PERF_MULTIPLE_INSTANCES:4

The query returned a single counter from each of multiple instances.

### -field PERF_COUNTERSET

The query returned multiple counters from each of multiple instances.

## -see-also

<a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_header">PERF_COUNTER_HEADER</a>



<a href="/windows/desktop/api/perflib/nf-perflib-perfquerycounterdata">PerfQueryCounterData</a>
