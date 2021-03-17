---
UID: NS:winperf._PERF_COUNTER_BLOCK
title: PERF_COUNTER_BLOCK (winperf.h)
description: Describes the block of memory that contains the raw performance counter data for an object's counters.
helpviewer_keywords: ["*PPERF_COUNTER_BLOCK","PERF_COUNTER_BLOCK","PERF_COUNTER_BLOCK structure [Perf]","_win32_perf_counter_block_str","base.perf_counter_block_str","perf.perf_counter_block_str","winperf/PERF_COUNTER_BLOCK"]
old-location: perf\perf_counter_block_str.htm
tech.root: perf
ms.assetid: 5cff6142-6d71-46a5-a943-3ec91ebac62b
ms.date: 12/05/2018
ms.keywords: '*PPERF_COUNTER_BLOCK, PERF_COUNTER_BLOCK, PERF_COUNTER_BLOCK structure [Perf], _win32_perf_counter_block_str, base.perf_counter_block_str, perf.perf_counter_block_str, winperf/PERF_COUNTER_BLOCK'
req.header: winperf.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: PERF_COUNTER_BLOCK, *PPERF_COUNTER_BLOCK
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PERF_COUNTER_BLOCK
 - winperf/_PERF_COUNTER_BLOCK
 - PPERF_COUNTER_BLOCK
 - winperf/PPERF_COUNTER_BLOCK
 - PERF_COUNTER_BLOCK
 - winperf/PERF_COUNTER_BLOCK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winperf.h
api_name:
 - PERF_COUNTER_BLOCK
---

# PERF_COUNTER_BLOCK structure


## -description

Describes the block of memory that contains the raw performance counter data for an 
object's counters.

## -struct-fields

### -field ByteLength

Size of this structure and the raw counter data that follows, in bytes.

## -remarks

The <b>CounterOffset</b> member of <a href="/windows/desktop/api/winperf/ns-winperf-perf_counter_definition">PERF_COUNTER_DEFINITION</a> provides the offset from the beginning of this structure to the counter value.

The location of the <b>PERF_COUNTER_BLOCK</b> structure within the <a href="/windows/desktop/api/winperf/ns-winperf-perf_object_type">PERF_OBJECT_TYPE</a> block depends on if the object contains instances. For details, see <a href="/windows/desktop/PerfCtrs/performance-data-format">Performance Data Format</a>.

You must ensure that the size of the counter block is aligned to an 8-byte boundary. For example, if the performance object includes two DWORD counters, you must add an additional four bytes to the counter block to make it aligned to an 8-byte boundary.

## -see-also

<a href="/windows/desktop/api/winperf/ns-winperf-perf_counter_definition">PERF_COUNTER_DEFINITION</a>



<a href="/windows/desktop/api/winperf/ns-winperf-perf_instance_definition">PERF_INSTANCE_DEFINITION</a>



<a href="/windows/desktop/api/winperf/ns-winperf-perf_object_type">PERF_OBJECT_TYPE</a>