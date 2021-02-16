---
UID: NS:minwinbase._CREATE_PROCESS_DEBUG_INFO
title: CREATE_PROCESS_DEBUG_INFO (minwinbase.h)
description: Contains process creation information that can be used by a debugger.
helpviewer_keywords: ["*LPCREATE_PROCESS_DEBUG_INFO","CREATE_PROCESS_DEBUG_INFO","CREATE_PROCESS_DEBUG_INFO structure","LPCREATE_PROCESS_DEBUG_INFO","LPCREATE_PROCESS_DEBUG_INFO structure pointer","_CREATE_PROCESS_DEBUG_INFO","_win32_create_process_debug_info_str","base.create_process_debug_info_str","minwinbase/CREATE_PROCESS_DEBUG_INFO","minwinbase/LPCREATE_PROCESS_DEBUG_INFO"]
old-location: base\create_process_debug_info_str.htm
tech.root: Debug
ms.assetid: 4607aaff-bd05-46b5-86ed-abfffe6c2551
ms.date: 12/05/2018
ms.keywords: '*LPCREATE_PROCESS_DEBUG_INFO, CREATE_PROCESS_DEBUG_INFO, CREATE_PROCESS_DEBUG_INFO structure, LPCREATE_PROCESS_DEBUG_INFO, LPCREATE_PROCESS_DEBUG_INFO structure pointer, _CREATE_PROCESS_DEBUG_INFO, _win32_create_process_debug_info_str, base.create_process_debug_info_str, minwinbase/CREATE_PROCESS_DEBUG_INFO, minwinbase/LPCREATE_PROCESS_DEBUG_INFO'
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
req.typenames: CREATE_PROCESS_DEBUG_INFO, *LPCREATE_PROCESS_DEBUG_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CREATE_PROCESS_DEBUG_INFO
 - minwinbase/_CREATE_PROCESS_DEBUG_INFO
 - LPCREATE_PROCESS_DEBUG_INFO
 - minwinbase/LPCREATE_PROCESS_DEBUG_INFO
 - CREATE_PROCESS_DEBUG_INFO
 - minwinbase/CREATE_PROCESS_DEBUG_INFO
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
 - CREATE_PROCESS_DEBUG_INFO
---

# CREATE_PROCESS_DEBUG_INFO structure


## -description

Contains process creation information that can be used by a debugger.

## -struct-fields

### -field hFile

A handle to the process's image file. If this member is <b>NULL</b>, the handle is not 
       valid. Otherwise, the debugger can use the member to read from and write to the image file.

When the debugger is finished with this file, it should close the handle using the 
       <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function.

### -field hProcess

A handle to the process. If this member is <b>NULL</b>, the handle is not valid. 
      Otherwise, the debugger can use the member to read from and write to the process's memory.

### -field hThread

A handle to the initial thread of the process identified by the <b>hProcess</b> member. 
      If <b>hThread</b> param is <b>NULL</b>, the handle is not valid. 
      Otherwise, the debugger has <b>THREAD_GET_CONTEXT</b>, 
      <b>THREAD_SET_CONTEXT</b>, and <b>THREAD_SUSPEND_RESUME</b> access to the 
      thread, allowing the debugger to read from and write to the registers of the thread and to control execution of 
      the thread.

### -field lpBaseOfImage

The base address of the executable image that the process is running.

### -field dwDebugInfoFileOffset

The offset to the debugging information in the file identified by the <b>hFile</b> 
      member.

### -field nDebugInfoSize

The size of the debugging information in the file, in bytes. If this value is zero, there is no debugging 
      information.

### -field lpThreadLocalBase

A pointer to a block of data. At offset 0x2C into this block is another pointer, called 
      <code>ThreadLocalStoragePointer</code>, that points to an array of per-module thread local storage 
      blocks. This gives a debugger access to per-thread data in the threads of the process being debugged using the 
      same algorithms that a compiler would use.

### -field lpStartAddress

A pointer to the starting address of the thread. This value may only be an approximation of the thread's 
      starting address, because any application with appropriate access to the thread can change the thread's context 
      by using the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadcontext">SetThreadContext</a> function.

### -field lpImageName

A pointer to the file name associated with the <b>hFile</b> member. This parameter may be 
       <b>NULL</b>, or it may contain the address of a string pointer in the address space of the 
       process being debugged. That address may, in turn, either be <b>NULL</b> or point to the 
       actual filename. If <b>fUnicode</b> is a nonzero value, the name string is Unicode; 
       otherwise, it is ANSI.

This member is strictly optional. Debuggers must be prepared to handle the case where 
       <b>lpImageName</b> is <b>NULL</b> or 
       *<b>lpImageName</b> (in the address space of the process being debugged) is 
       <b>NULL</b>. Specifically, the system does not provide an image name for a create process 
       event, and will not likely pass an image name for the first DLL event. The system also does not provide this 
       information in the case of debug events that originate from a call to the 
       <a href="/windows/desktop/api/debugapi/nf-debugapi-debugactiveprocess">DebugActiveProcess</a> function.

### -field fUnicode

A value that indicates whether a file name specified by the <b>lpImageName</b> member 
      is Unicode or ANSI. A nonzero value indicates Unicode; zero indicates ANSI.

## -see-also

<a href="/windows/desktop/api/minwinbase/ns-minwinbase-create_thread_debug_info">CREATE_THREAD_DEBUG_INFO</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-debug_event">DEBUG_EVENT</a>



<a href="/windows/desktop/api/debugapi/nf-debugapi-debugactiveprocess">DebugActiveProcess</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-load_dll_debug_info">LOAD_DLL_DEBUG_INFO</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadcontext">SetThreadContext</a>