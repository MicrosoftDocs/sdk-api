---
UID: NS:minwinbase._CREATE_THREAD_DEBUG_INFO
title: "_CREATE_THREAD_DEBUG_INFO"
author: windows-sdk-content
description: Contains thread-creation information that can be used by a debugger.
old-location: base\create_thread_debug_info_str.htm
tech.root: debug
ms.assetid: daabd118-fa03-410e-af25-8655194902b0
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: "*LPCREATE_THREAD_DEBUG_INFO, CREATE_THREAD_DEBUG_INFO, CREATE_THREAD_DEBUG_INFO structure, LPCREATE_THREAD_DEBUG_INFO, LPCREATE_THREAD_DEBUG_INFO structure pointer, _CREATE_THREAD_DEBUG_INFO, _win32_create_thread_debug_info_str, base.create_thread_debug_info_str, minwinbase/CREATE_THREAD_DEBUG_INFO, minwinbase/LPCREATE_THREAD_DEBUG_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - minwinbase.h
api_name:
 - CREATE_THREAD_DEBUG_INFO
product: Windows
targetos: Windows
req.typenames: CREATE_THREAD_DEBUG_INFO, *LPCREATE_THREAD_DEBUG_INFO
req.redist: 
---

# _CREATE_THREAD_DEBUG_INFO structure


## -description


Contains thread-creation information that can be used by a debugger.


## -struct-fields




### -field hThread

A handle to the thread whose creation caused the debugging event. If this member is <b>NULL</b>, the handle is not valid. Otherwise, the debugger has THREAD_GET_CONTEXT, THREAD_SET_CONTEXT, and THREAD_SUSPEND_RESUME access to the thread, allowing the debugger to read from and write to the registers of the thread and control execution of the thread.


### -field lpThreadLocalBase

A pointer to a block of data. At offset 0x2C into this block is another pointer, called ThreadLocalStoragePointer, that points to an array of per-module thread local storage blocks. This gives a debugger access to per-thread data in the threads of the process being debugged using the same algorithms that a compiler would use.


### -field lpStartAddress

A pointer to the starting address of the thread. This value may only be an approximation of the thread's starting address, because any application with appropriate access to the thread can change the thread's context by using the 
<a href="https://msdn.microsoft.com/be134953-b569-48ea-80ac-ab14dee24500">SetThreadContext</a> function.


## -see-also




<a href="https://msdn.microsoft.com/4607aaff-bd05-46b5-86ed-abfffe6c2551">CREATE_PROCESS_DEBUG_INFO</a>



<a href="https://msdn.microsoft.com/056aa7ee-51ca-48ec-9cd7-26085bb85b11">DEBUG_EVENT</a>



<a href="https://msdn.microsoft.com/bf1294cd-1836-49d3-9cc4-4532429a301f">Debugging Structures</a>



<a href="https://msdn.microsoft.com/80edb12f-1d1f-4480-9032-5f7a17f47910">LOAD_DLL_DEBUG_INFO</a>



<a href="https://msdn.microsoft.com/be134953-b569-48ea-80ac-ab14dee24500">SetThreadContext</a>
 

 

