---
UID: NS:minidumpapiset._MINIDUMP_THREAD_EX
title: MINIDUMP_THREAD_EX (minidumpapiset.h)
description: Contains extended information for a specific thread.
helpviewer_keywords: ["*PMINIDUMP_THREAD_EX","MINIDUMP_THREAD_EX","MINIDUMP_THREAD_EX structure","PMINIDUMP_THREAD_EX","PMINIDUMP_THREAD_EX structure pointer","_MINIDUMP_THREAD_EX","_win32_minidump_thread_ex_str","base.minidump_thread_ex_str","minidumpapiset/MINIDUMP_THREAD_EX","minidumpapiset/PMINIDUMP_THREAD_EX"]
old-location: base\minidump_thread_ex_str.htm
tech.root: Debug
ms.assetid: aa99bdf3-29b7-4865-8935-810388f3d2b3
ms.date: 12/05/2018
ms.keywords: '*PMINIDUMP_THREAD_EX, MINIDUMP_THREAD_EX, MINIDUMP_THREAD_EX structure, PMINIDUMP_THREAD_EX, PMINIDUMP_THREAD_EX structure pointer, _MINIDUMP_THREAD_EX, _win32_minidump_thread_ex_str, base.minidump_thread_ex_str, minidumpapiset/MINIDUMP_THREAD_EX, minidumpapiset/PMINIDUMP_THREAD_EX'
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
targetos: Windows
req.typenames: MINIDUMP_THREAD_EX, *PMINIDUMP_THREAD_EX
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - _MINIDUMP_THREAD_EX
 - minidumpapiset/_MINIDUMP_THREAD_EX
 - PMINIDUMP_THREAD_EX
 - minidumpapiset/PMINIDUMP_THREAD_EX
 - MINIDUMP_THREAD_EX
 - minidumpapiset/MINIDUMP_THREAD_EX
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - minidumpapiset.h
api_name:
 - MINIDUMP_THREAD_EX
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
<a href="/windows/desktop/ProcThread/scheduling-priorities">Scheduling Priorities</a>.

### -field Priority

The priority level of the thread.

### -field Teb

The thread environment block.

### -field Stack

A 
<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_memory_descriptor">MINIDUMP_MEMORY_DESCRIPTOR</a> structure.

### -field ThreadContext

A 
<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_location_descriptor">MINIDUMP_LOCATION_DESCRIPTOR</a> structure.

### -field BackingStore

<b>Intel Itanium:  </b>The backing store for the thread.

## -see-also

<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_location_descriptor">MINIDUMP_LOCATION_DESCRIPTOR</a>



<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_memory_descriptor">MINIDUMP_MEMORY_DESCRIPTOR</a>