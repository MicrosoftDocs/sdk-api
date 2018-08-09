---
UID: NS:perflib._PROVIDER_CONTEXT
title: "_PROVIDER_CONTEXT"
author: windows-sdk-content
description: Defines provider context information.
old-location: perf\perf_provider_context.htm
old-project: PerfCtrs
ms.assetid: 9bfab8aa-f44b-4515-8a2a-764583080f57
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: "*PPERF_PROVIDER_CONTEXT, PERF_PROVIDER_CONTEXT, PERF_PROVIDER_CONTEXT structure [Perf], PPERF_PROVIDER_CONTEXT, PPERF_PROVIDER_CONTEXT structure pointer [Perf], _PROVIDER_CONTEXT, perf.perf_provider_context, perflib/PERF_PROVIDER_CONTEXT, perflib/PPERF_PROVIDER_CONTEXT"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: PERF_PROVIDER_CONTEXT, *PPERF_PROVIDER_CONTEXT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Perflib.h
api_name:
 - PERF_PROVIDER_CONTEXT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _PROVIDER_CONTEXT structure


## -description


Defines provider context information.


## -struct-fields




### -field ContextSize

The size of this structure.


### -field Reserved

Reserved.


### -field ControlCallback

The name of the <a href="https://msdn.microsoft.com/0f771ab7-af42-481b-b2da-20dcdf49b82b">ControlCallback</a> function that PERFLIB calls to notify you of consumer requests, such as a request to add or remove counters from the query. Set this member if the <b>callback</b> attribute of the <a href="https://msdn.microsoft.com/library/windows/hardware/hh406455">provider</a> element is "custom" or you used the <b>-NotificationCallback</b> argument when calling <a href="https://msdn.microsoft.com/3939f6a1-0a94-429d-a71e-b37f045fea13">CTRPP</a>. Otherwise, <b>NULL</b>. 


### -field MemAllocRoutine

The name of the <a href="https://msdn.microsoft.com/09af7e56-2174-4a82-b45b-59f4180e4aab">AllocateMemory</a> function that PERFLIB calls to allocate memory. Set this member if you used the <b>-MemoryRoutines</b> argument when calling <a href="https://msdn.microsoft.com/3939f6a1-0a94-429d-a71e-b37f045fea13">CTRPP</a>. Otherwise, <b>NULL</b>. 


### -field MemFreeRoutine

The name of the <a href="https://msdn.microsoft.com/3b2f9f68-131a-4e17-8b43-6c3a20871dad">FreeMemory</a> function that PERFLIB calls to free memory allocated by the <a href="https://msdn.microsoft.com/09af7e56-2174-4a82-b45b-59f4180e4aab">AllocateMemory</a> function. Must be <b>NULL</b> if <b>MemAllocRoutine</b> is <b>NULL</b>.


### -field pMemContext

Context information passed to the memory allocation and free routines. Can be <b>NULL</b>.


## -remarks



By default, PERFLIB uses process heap. The memory allocation and free routines lets you provide custom memory management. 




## -see-also




<a href="https://msdn.microsoft.com/9f3aefbf-0836-46fc-8a53-858c3c94cef9">PerfStartProviderEx</a>
 

 

