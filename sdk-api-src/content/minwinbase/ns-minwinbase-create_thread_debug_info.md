---
UID: NS:minwinbase._CREATE_THREAD_DEBUG_INFO
title: CREATE_THREAD_DEBUG_INFO (minwinbase.h)
description: Contains thread-creation information that can be used by a debugger.
helpviewer_keywords: ["*LPCREATE_THREAD_DEBUG_INFO","CREATE_THREAD_DEBUG_INFO","CREATE_THREAD_DEBUG_INFO structure","LPCREATE_THREAD_DEBUG_INFO","LPCREATE_THREAD_DEBUG_INFO structure pointer","_CREATE_THREAD_DEBUG_INFO","_win32_create_thread_debug_info_str","base.create_thread_debug_info_str","minwinbase/CREATE_THREAD_DEBUG_INFO","minwinbase/LPCREATE_THREAD_DEBUG_INFO"]
old-location: base\create_thread_debug_info_str.htm
tech.root: Debug
ms.assetid: daabd118-fa03-410e-af25-8655194902b0
ms.date: 12/05/2018
ms.keywords: '*LPCREATE_THREAD_DEBUG_INFO, CREATE_THREAD_DEBUG_INFO, CREATE_THREAD_DEBUG_INFO structure, LPCREATE_THREAD_DEBUG_INFO, LPCREATE_THREAD_DEBUG_INFO structure pointer, _CREATE_THREAD_DEBUG_INFO, _win32_create_thread_debug_info_str, base.create_thread_debug_info_str, minwinbase/CREATE_THREAD_DEBUG_INFO, minwinbase/LPCREATE_THREAD_DEBUG_INFO'
req.header: minwinbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: CREATE_THREAD_DEBUG_INFO, *LPCREATE_THREAD_DEBUG_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CREATE_THREAD_DEBUG_INFO
 - minwinbase/_CREATE_THREAD_DEBUG_INFO
 - LPCREATE_THREAD_DEBUG_INFO
 - minwinbase/LPCREATE_THREAD_DEBUG_INFO
 - CREATE_THREAD_DEBUG_INFO
 - minwinbase/CREATE_THREAD_DEBUG_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - minwinbase.h
api_name:
 - CREATE_THREAD_DEBUG_INFO
---

# CREATE_THREAD_DEBUG_INFO structure


## -description

Contains thread-creation information that can be used by a debugger.

## -struct-fields

### -field hThread

A handle to the thread whose creation caused the debugging event. If this member is <b>NULL</b>, the handle is not valid. Otherwise, the debugger has THREAD_GET_CONTEXT, THREAD_SET_CONTEXT, and THREAD_SUSPEND_RESUME access to the thread, allowing the debugger to read from and write to the registers of the thread and control execution of the thread.

### -field lpThreadLocalBase

A pointer to a block of data. At offset 0x2C into this block is another pointer, called ThreadLocalStoragePointer, that points to an array of per-module thread local storage blocks. This gives a debugger access to per-thread data in the threads of the process being debugged using the same algorithms that a compiler would use.

### -field lpStartAddress

A pointer to the starting address of the thread. This value may only be an approximation of the thread's starting address, because any application with appropriate access to the thread can change the thread's context by using the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadcontext">SetThreadContext</a> function.

## -see-also

<a href="/windows/desktop/api/minwinbase/ns-minwinbase-create_process_debug_info">CREATE_PROCESS_DEBUG_INFO</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-debug_event">DEBUG_EVENT</a>



<a href="/windows/desktop/Debug/debugging-structures">Debugging Structures</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-load_dll_debug_info">LOAD_DLL_DEBUG_INFO</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadcontext">SetThreadContext</a>