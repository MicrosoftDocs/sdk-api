---
UID: NF:perflib.PerfDeleteCounters
title: PerfDeleteCounters function (perflib.h)
description: Removes the specified performance counter specifications from the specified query.
helpviewer_keywords: ["PerfDeleteCounters","PerfDeleteCounters function [Perf]","perf.perfdeletecounters","perflib/PerfDeleteCounters"]
old-location: perf\perfdeletecounters.htm
tech.root: perf
ms.assetid: 330CA041-41CA-4C48-B88B-C48A0143505E
ms.date: 12/05/2018
ms.keywords: PerfDeleteCounters, PerfDeleteCounters function [Perf], perf.perfdeletecounters, perflib/PerfDeleteCounters
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
 - PerfDeleteCounters
 - perflib/PerfDeleteCounters
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
 - PerfDeleteCounters
---

# PerfDeleteCounters function


## -description

Removes the specified performance counter specifications from the specified query.

## -parameters

### -param hQuery [in]

A handle to the query from which you want to remove performance counter specifications.

### -param pCounters [in, out]

A pointer to the performance counter specifications that you want to remove.

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

Configure each <a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_identifier">PERF_COUNTER_IDENTIFIER</a> block in the same way as described in the Remarks for <a href="/windows/desktop/api/perflib/nf-perflib-perfaddcounters">PerfAddCounters</a>.



<b>PerfDeleteCounters</b> attempts to remove one counter specification from the
query for each <a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_identifier">PERF_COUNTER_IDENTIFIER</a> block,  and updates the <b>Status</b> member of the <b>PERF_COUNTER_IDENTIFIER</b> structure in each
block with the result of the attempt.

## -see-also

<a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_identifier">PERF_COUNTER_IDENTIFIER</a>



<a href="/windows/desktop/api/perflib/nf-perflib-perfaddcounters">PerfAddCounters</a>