---
UID: NS:minidumpapiset._MINIDUMP_THREAD_EX
title: MINIDUMP_THREAD_EX (minidumpapiset.h)
author: windows-sdk-content
description: Contains extended information for a specific thread.
old-location: base\minidump_thread_ex_str.htm
tech.root: Debug
ms.assetid: aa99bdf3-29b7-4865-8935-810388f3d2b3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PMINIDUMP_THREAD_EX, MINIDUMP_THREAD_EX, MINIDUMP_THREAD_EX structure, PMINIDUMP_THREAD_EX, PMINIDUMP_THREAD_EX structure pointer, _MINIDUMP_THREAD_EX, _win32_minidump_thread_ex_str, base.minidump_thread_ex_str, minidumpapiset/MINIDUMP_THREAD_EX, minidumpapiset/PMINIDUMP_THREAD_EX"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - minidumpapiset.h
api_name:
 - MINIDUMP_THREAD_EX
product: Windows
targetos: Windows
req.typenames: MINIDUMP_THREAD_EX, *PMINIDUMP_THREAD_EX
req.redist: DbgHelp.dll 5.1 or later
---

# MINIDUMP_THREAD_EX structure


## -description


Contains extended information for a specific thread.


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
<a href="https://msdn.microsoft.com/en-us/library/ms680384(v=VS.85).aspx">MINIDUMP_MEMORY_DESCRIPTOR</a> structure.


### -field ThreadContext

A 
<a href="https://msdn.microsoft.com/en-us/library/ms680383(v=VS.85).aspx">MINIDUMP_LOCATION_DESCRIPTOR</a> structure.


### -field BackingStore

<b>Intel Itanium:  </b>The backing store for the thread.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms680383(v=VS.85).aspx">MINIDUMP_LOCATION_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/en-us/library/ms680384(v=VS.85).aspx">MINIDUMP_MEMORY_DESCRIPTOR</a>
 

 

