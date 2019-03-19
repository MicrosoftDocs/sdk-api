---
UID: NC:perflib.PERF_MEM_FREE
title: PERF_MEM_FREE (perflib.h)
author: windows-sdk-content
description: Providers implement this function to provide custom memory management for PERFLIB.
old-location: perf\freememory.htm
tech.root: perfctrs
ms.assetid: 3b2f9f68-131a-4e17-8b43-6c3a20871dad
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FreeMemory, FreeMemory callback function [Perf], PERF_MEM_FREE, PERF_MEM_FREE callback, perf.freememory, perflib/FreeMemory
ms.topic: callback
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
---

# PERF_MEM_FREE callback function


## -description


Providers implement this function to provide custom memory management for PERFLIB. PERFLIB calls this callback when it needs to free memory that it allocated using <a href="https://msdn.microsoft.com/09af7e56-2174-4a82-b45b-59f4180e4aab">AllocateMemory</a>. 

The <b>PERF_MEM_FREE</b> type defines a pointer to this callback function. The <b>FreeMemory</b> function is a placeholder for the application-defined function name.


## -parameters




### -param pBuffer [in]

Memory to free.


### -param pContext [in]

Context information set in the <b>pMemContext</b> member of <a href="https://msdn.microsoft.com/9bfab8aa-f44b-4515-8a2a-764583080f57">PERF_PROVIDER_CONTEXT</a>.


## -returns



This callback function does not return a value.




## -remarks



If you used the <b>-MemoryRoutines</b> when calling <a href="https://msdn.microsoft.com/3939f6a1-0a94-429d-a71e-b37f045fea13">CTRPP</a>, you must implement this callback function. You pass the name of your callback function to <a href="https://msdn.microsoft.com/edcf8df3-0f6d-4849-b41d-270509499b8e">CounterInitialize</a>.

<b>Windows Vista:  </b>The <a href="https://msdn.microsoft.com/edcf8df3-0f6d-4849-b41d-270509499b8e">CounterInitialize</a> function is named <b>PerfAutoInitialize</b>.




## -see-also




<a href="https://msdn.microsoft.com/09af7e56-2174-4a82-b45b-59f4180e4aab">AllocateMemory</a>



<a href="https://msdn.microsoft.com/9bfab8aa-f44b-4515-8a2a-764583080f57">PERF_PROVIDER_CONTEXT</a>
 

 

