---
UID: NS:perflib._STRING_COUNTER_HEADER
title: PERF_STRING_COUNTER_HEADER (perflib.h)
description: Indicates where in the PERF_STRING_BUFFER_HEADER block that the string that contains the name or help string for the indicated performance counter starts.helpviewer_keywords: ["*PPERF_STRING_COUNTER_HEADER","PERF_STRING_COUNTER_HEADER","PERF_STRING_COUNTER_HEADER structure [Perf]","PPERF_STRING_COUNTER_HEADER","PPERF_STRING_COUNTER_HEADER structure pointer [Perf]","perf.perf_string_counter_header","perflib/PERF_STRING_COUNTER_HEADER","perflib/PPERF_STRING_COUNTER_HEADER"]
old-location: perf\perf_string_counter_header.htm
tech.root: perfctrs
ms.assetid: 73DFA1C0-B0E8-4788-8CBA-1CFA7580F633
ms.date: 12/05/2018
ms.keywords: '*PPERF_STRING_COUNTER_HEADER, PERF_STRING_COUNTER_HEADER, PERF_STRING_COUNTER_HEADER structure [Perf], PPERF_STRING_COUNTER_HEADER, PPERF_STRING_COUNTER_HEADER structure pointer [Perf], perf.perf_string_counter_header, perflib/PERF_STRING_COUNTER_HEADER, perflib/PPERF_STRING_COUNTER_HEADER'
f1_keywords:
- perflib/PERF_STRING_COUNTER_HEADER
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Perflib.h
api_name:
- PERF_STRING_COUNTER_HEADER
targetos: Windows
req.typenames: PERF_STRING_COUNTER_HEADER, *PPERF_STRING_COUNTER_HEADER
req.redist: 
ms.custom: 19H1
---

# PERF_STRING_COUNTER_HEADER structure


## -description


Indicates where in the <a href="https://docs.microsoft.com/windows/win32/api/perflib/ns-perflib-perf_string_buffer_header">PERF_STRING_BUFFER_HEADER</a> block that the string that contains the name or help string  for the indicated performance counter starts. The <b>PERF_STRING_COUNTER_HEADER</b> structure is part of the
<a href="https://docs.microsoft.com/windows/win32/api/perflib/ns-perflib-perf_string_buffer_header">PERF_STRING_BUFFER_HEADER</a> block


## -struct-fields




### -field dwCounterId

The identifier of the  performance counter.


### -field dwOffset

The number of bytes from the start of the
<a href="https://docs.microsoft.com/windows/win32/api/perflib/ns-perflib-perf_string_buffer_header">PERF_STRING_BUFFER_HEADER</a> block to the null-terminated UTF-16LE data. A value of 0xFFFFFFFF indicates that the string is not present; in other words, that the value of the string is NULL.


## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/api/perflib/nf-perflib-perfquerycountersetregistrationinfo">PerfQueryCounterSetRegistrationInfo</a> function called with the <i>requestCode</i> parameter set to
<b>PERF_REG_COUNTER_NAME_STRINGS</b> or <b>PERF_REG_COUNTER_HELP_STRINGS</b> gets a
<a href="https://docs.microsoft.com/windows/win32/api/perflib/ns-perflib-perf_string_buffer_header">PERF_STRING_BUFFER_HEADER</a> block that contains one or more
<b>PERF_STRING_COUNTER_HEADER</b> structures.




## -see-also




<a href="https://docs.microsoft.com/windows/win32/api/perflib/ns-perflib-perf_string_buffer_header">PERF_STRING_BUFFER_HEADER</a>



<a href="https://docs.microsoft.com/windows/desktop/api/perflib/nf-perflib-perfquerycountersetregistrationinfo">PerfQueryCounterSetRegistrationInfo</a>
 

 

