---
UID: NS:perflib._STRING_BUFFER_HEADER
title: PERF_STRING_BUFFER_HEADER (perflib.h)
description: Provides information about the PERF_STRING_BUFFER_HEADER block that contains the structure.
helpviewer_keywords: ["*PPERF_STRING_BUFFER_HEADER","PERF_STRING_BUFFER_HEADER","PERF_STRING_BUFFER_HEADER structure [Perf]","PPERF_STRING_BUFFER_HEADER","PPERF_STRING_BUFFER_HEADER structure pointer [Perf]","perf.perf_string_buffer_header","perflib/PERF_STRING_BUFFER_HEADER","perflib/PPERF_STRING_BUFFER_HEADER"]
old-location: perf\perf_string_buffer_header.htm
tech.root: perf
ms.assetid: 874A97BA-708E-4001-A7CA-1C3114577D7D
ms.date: 12/05/2018
ms.keywords: '*PPERF_STRING_BUFFER_HEADER, PERF_STRING_BUFFER_HEADER, PERF_STRING_BUFFER_HEADER structure [Perf], PPERF_STRING_BUFFER_HEADER, PPERF_STRING_BUFFER_HEADER structure pointer [Perf], perf.perf_string_buffer_header, perflib/PERF_STRING_BUFFER_HEADER, perflib/PPERF_STRING_BUFFER_HEADER'
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
req.typenames: PERF_STRING_BUFFER_HEADER, *PPERF_STRING_BUFFER_HEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _STRING_BUFFER_HEADER
 - perflib/_STRING_BUFFER_HEADER
 - PPERF_STRING_BUFFER_HEADER
 - perflib/PPERF_STRING_BUFFER_HEADER
 - PERF_STRING_BUFFER_HEADER
 - perflib/PERF_STRING_BUFFER_HEADER
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
 - PERF_STRING_BUFFER_HEADER
---

# PERF_STRING_BUFFER_HEADER structure


## -description

Provides information about the <b>PERF_STRING_BUFFER_HEADER</b> block that contains the structure. The <b>PERF_STRING_BUFFER_HEADER</b> block provides the names or help strings for the performance counters in a counter set, amd consists of the following items in order:<ol>
<li>A <b>PERF_STRING_BUFFER_HEADER</b> structure</li>
<li>A number of <a href="/windows/win32/api/perflib/ns-perflib-perf_string_counter_header">PERF_STRING_COUNTER_HEADER</a> structures. The <b>dwCounters</b> member of the <b>PERF_STRING_BUFFER_HEADER</b> structure specifies how many <b>PERF_STRING_COUNTER_HEADER</b> structures the <b>PERF_STRING_BUFFER_HEADER</b> block contains.</li>
<li>A block of string data.</li>
</ol>

## -struct-fields

### -field dwSize

The total size of the <b>PERF_STRING_BUFFER_HEADER</b> block, in bytes. This total size is the sum of the sizes of the <b>PERF_STRING_BUFFER_HEADER</b> structure, all of the <a href="/windows/win32/api/perflib/ns-perflib-perf_string_counter_header">PERF_STRING_COUNTER_HEADER</a> structures, and the block of string data.

### -field dwCounters

The number of <a href="/windows/win32/api/perflib/ns-perflib-perf_string_counter_header">PERF_STRING_COUNTER_HEADER</a> structures in the  <b>PERF_STRING_BUFFER_HEADER</b> block.

## -remarks

The <a href="/windows/desktop/api/perflib/nf-perflib-perfquerycountersetregistrationinfo">PerfQueryCounterSetRegistrationInfo</a> function called with the <i>requestCode</i> parameter set to
<b>PERF_REG_COUNTER_NAME_STRINGS</b> or <b>PERF_REG_COUNTER_HELP_STRINGS</b> gets a
<b>PERF_STRING_BUFFER_HEADER</b> block.

## -see-also

<a href="/windows/win32/api/perflib/ns-perflib-perf_string_counter_header">PERF_STRING_COUNTER_HEADER</a>



<a href="/windows/desktop/api/perflib/nf-perflib-perfquerycountersetregistrationinfo">PerfQueryCounterSetRegistrationInfo</a>