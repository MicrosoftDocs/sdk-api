---
UID: NC:perflib.PERF_MEM_FREE
title: PERF_MEM_FREE (perflib.h)
author: windows-sdk-content
description: Providers implement this function to provide custom memory management for PERFLIB.
old-location: perf\freememory.htm
tech.root: perfctrs
ms.assetid: 3b2f9f68-131a-4e17-8b43-6c3a20871dad
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FreeMemory, FreeMemory callback function [Perf], PERF_MEM_FREE, PERF_MEM_FREE callback, perf.freememory, perflib/FreeMemory
ms.topic: callback
f1_keywords: 
 - "perflib/FreeMemory"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Perflib.h
api_name:
 - FreeMemory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PERF_MEM_FREE callback function


## -description


Providers implement this function to provide custom memory management for PERFLIB. PERFLIB calls this callback when it needs to free memory that it allocated using <a href="https://docs.microsoft.com/windows/desktop/api/perflib/nc-perflib-perf_mem_alloc">AllocateMemory</a>. 

The <b>PERF_MEM_FREE</b> type defines a pointer to this callback function. The <b>FreeMemory</b> function is a placeholder for the application-defined function name.


## -parameters




### -param pBuffer [in]

Memory to free.


### -param pContext [in]

Context information set in the <b>pMemContext</b> member of <a href="https://docs.microsoft.com/windows/win32/api/perflib/ns-perflib-perf_provider_context">PERF_PROVIDER_CONTEXT</a>.


## -returns



This callback function does not return a value.




## -remarks



If you used the <b>-MemoryRoutines</b> when calling <a href="https://docs.microsoft.com/windows/desktop/PerfCtrs/ctrpp">CTRPP</a>, you must implement this callback function. You pass the name of your callback function to <a href="https://docs.microsoft.com/windows/desktop/PerfCtrs/counterinitialize">CounterInitialize</a>.

<b>Windows Vista:  </b>The <a href="https://docs.microsoft.com/windows/desktop/PerfCtrs/counterinitialize">CounterInitialize</a> function is named <b>PerfAutoInitialize</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/perflib/nc-perflib-perf_mem_alloc">AllocateMemory</a>



<a href="https://docs.microsoft.com/windows/win32/api/perflib/ns-perflib-perf_provider_context">PERF_PROVIDER_CONTEXT</a>
 

 

