---
UID: NS:minidumpapiset._MINIDUMP_THREAD
title: "_MINIDUMP_THREAD"
author: windows-sdk-content
description: Contains information for a specific thread.
old-location: base\minidump_thread_str.htm
old-project: Debug
ms.assetid: 07d4ba98-e74d-4f50-9afa-d09d93da3d6b
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: "*PMINIDUMP_THREAD, MINIDUMP_THREAD, MINIDUMP_THREAD structure, PMINIDUMP_THREAD, PMINIDUMP_THREAD structure pointer, _MINIDUMP_THREAD, _win32_minidump_thread_str, base.minidump_thread_str, minidumpapiset/MINIDUMP_THREAD, minidumpapiset/PMINIDUMP_THREAD"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: minidumpapiset.h
req.include-header: DbgHelp.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: MINIDUMP_THREAD, *PMINIDUMP_THREAD
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	minidumpapiset.h
api_name:
-	MINIDUMP_THREAD
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MINIDUMP_THREAD structure


## -description


Contains information for a specific thread.


## -struct-fields




### -field ThreadId

The identifier of the thread.


### -field SuspendCount

The suspend count for the thread. If the suspend count is greater than zero, the thread is suspended; otherwise, the thread is not suspended. The maximum value is MAXIMUM_SUSPEND_COUNT.


### -field PriorityClass

The priority class of the thread. See 
<a href="https://msdn.microsoft.com/8710cd56-6bf3-4317-a1f6-1a159394ce2a">Scheduling Priorities</a>.


### -field Priority

The priority level of the thread.


### -field Teb

The thread environment block.


### -field Stack

A 
<a href="https://msdn.microsoft.com/34c6de99-8ba5-4199-a382-3e3f7d02571f">MINIDUMP_MEMORY_DESCRIPTOR</a> structure.


### -field ThreadContext

A 
<a href="https://msdn.microsoft.com/aef17239-9b56-4d49-8347-610270f8612b">MINIDUMP_LOCATION_DESCRIPTOR</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/aef17239-9b56-4d49-8347-610270f8612b">MINIDUMP_LOCATION_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/34c6de99-8ba5-4199-a382-3e3f7d02571f">MINIDUMP_MEMORY_DESCRIPTOR</a>
 

 

