---
UID: NS:perflib._PROVIDER_CONTEXT
title: PERF_PROVIDER_CONTEXT (perflib.h)
description: Defines provider context information.
helpviewer_keywords: ["*PPERF_PROVIDER_CONTEXT","PERF_PROVIDER_CONTEXT","PERF_PROVIDER_CONTEXT structure [Perf]","PPERF_PROVIDER_CONTEXT","PPERF_PROVIDER_CONTEXT structure pointer [Perf]","perf.perf_provider_context","perflib/PERF_PROVIDER_CONTEXT","perflib/PPERF_PROVIDER_CONTEXT"]
old-location: perf\perf_provider_context.htm
tech.root: perf
ms.assetid: 9bfab8aa-f44b-4515-8a2a-764583080f57
ms.date: 12/05/2018
ms.keywords: '*PPERF_PROVIDER_CONTEXT, PERF_PROVIDER_CONTEXT, PERF_PROVIDER_CONTEXT structure [Perf], PPERF_PROVIDER_CONTEXT, PPERF_PROVIDER_CONTEXT structure pointer [Perf], perf.perf_provider_context, perflib/PERF_PROVIDER_CONTEXT, perflib/PPERF_PROVIDER_CONTEXT'
req.header: perflib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: PERF_PROVIDER_CONTEXT, *PPERF_PROVIDER_CONTEXT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PROVIDER_CONTEXT
 - perflib/_PROVIDER_CONTEXT
 - PPERF_PROVIDER_CONTEXT
 - perflib/PPERF_PROVIDER_CONTEXT
 - PERF_PROVIDER_CONTEXT
 - perflib/PERF_PROVIDER_CONTEXT
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
 - PERF_PROVIDER_CONTEXT
---

# PERF_PROVIDER_CONTEXT structure


## -description

Defines provider context information.

## -struct-fields

### -field ContextSize

The size of this structure.

### -field Reserved

Reserved.

### -field ControlCallback

The name of the <a href="/windows/desktop/api/perflib/nc-perflib-perflibrequest">ControlCallback</a> function that PERFLIB calls to notify you of consumer requests, such as a request to add or remove counters from the query. Set this member if the <b>callback</b> attribute of the <a href="/previous-versions/aa373164(v=vs.85)">provider</a> element is "custom" or you used the <b>-NotificationCallback</b> argument when calling <a href="/windows/desktop/PerfCtrs/ctrpp">CTRPP</a>. Otherwise, <b>NULL</b>.

### -field MemAllocRoutine

The name of the <a href="/windows/desktop/api/perflib/nc-perflib-perf_mem_alloc">AllocateMemory</a> function that PERFLIB calls to allocate memory. Set this member if you used the <b>-MemoryRoutines</b> argument when calling <a href="/windows/desktop/PerfCtrs/ctrpp">CTRPP</a>. Otherwise, <b>NULL</b>.

### -field MemFreeRoutine

The name of the <a href="/windows/desktop/api/perflib/nc-perflib-perf_mem_free">FreeMemory</a> function that PERFLIB calls to free memory allocated by the <a href="/windows/desktop/api/perflib/nc-perflib-perf_mem_alloc">AllocateMemory</a> function. Must be <b>NULL</b> if <b>MemAllocRoutine</b> is <b>NULL</b>.

### -field pMemContext

Context information passed to the memory allocation and free routines. Can be <b>NULL</b>.

## -remarks

By default, PERFLIB uses process heap. The memory allocation and free routines lets you provide custom memory management.

## -see-also

<a href="/windows/desktop/api/perflib/nf-perflib-perfstartproviderex">PerfStartProviderEx</a>