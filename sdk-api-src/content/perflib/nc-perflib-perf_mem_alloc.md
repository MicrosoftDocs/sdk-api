---
UID: NC:perflib.PERF_MEM_ALLOC
title: PERF_MEM_ALLOC (perflib.h)
description: Providers implement this function to provide custom memory management for PERFLIB.A
helpviewer_keywords: ["AllocateMemory","AllocateMemory callback function [Perf]","PERF_MEM_ALLOC","PERF_MEM_ALLOC callback","perf.allocatememory","perflib/AllocateMemory"]
old-location: perf\allocatememory.htm
tech.root: perf
ms.assetid: 09af7e56-2174-4a82-b45b-59f4180e4aab
ms.date: 12/05/2018
ms.keywords: AllocateMemory, AllocateMemory callback function [Perf], PERF_MEM_ALLOC, PERF_MEM_ALLOC callback, perf.allocatememory, perflib/AllocateMemory
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PERF_MEM_ALLOC
 - perflib/PERF_MEM_ALLOC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Perflib.h
api_name:
 - AllocateMemory
---

# PERF_MEM_ALLOC callback function


## -description

Providers implement this function to provide custom memory management for PERFLIB. PERFLIB calls this callback when it needs to allocate memory. By default, PERFLIB uses the process heap to allocate memory.

The <b>PERF_MEM_ALLOC</b> type defines a pointer to this callback function. The <b>AllocateMemory</b> function is a placeholder for the application-defined function name.

## -parameters

### -param AllocSize [in]

Number of bytes to allocate.

### -param pContext [in]

Context information set in the <b>pMemContext</b> member of <a href="/windows/win32/api/perflib/ns-perflib-perf_provider_context">PERF_PROVIDER_CONTEXT</a>.

## -returns

Pointer to the allocated memory or <b>NULL</b> if an error occurred.

## -remarks

If you used the <b>-MemoryRoutines</b> when calling <a href="/windows/desktop/PerfCtrs/ctrpp">CTRPP</a>, you must implement this callback function. You pass the name of your callback function to <a href="/windows/desktop/PerfCtrs/counterinitialize">CounterInitialize</a>.

<b>Windows Vista:  </b>The <a href="/windows/desktop/PerfCtrs/counterinitialize">CounterInitialize</a> function is named <b>PerfAutoInitialize</b>.

## -see-also

<a href="/windows/desktop/api/perflib/nc-perflib-perf_mem_free">FreeMemory</a>



<a href="/windows/win32/api/perflib/ns-perflib-perf_provider_context">PERF_PROVIDER_CONTEXT</a>
