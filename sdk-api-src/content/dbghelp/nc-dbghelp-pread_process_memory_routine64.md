---
UID: NC:dbghelp.PREAD_PROCESS_MEMORY_ROUTINE64
title: PREAD_PROCESS_MEMORY_ROUTINE64 (dbghelp.h)
description: PREAD_PROCESS_MEMORY_ROUTINE64 (dbghelp.h) is an application-defined callback function used with the StackWalk64 function.
helpviewer_keywords: ["PREAD_PROCESS_MEMORY_ROUTINE","PREAD_PROCESS_MEMORY_ROUTINE64","ReadProcessMemoryProc64","ReadProcessMemoryProc64 callback","ReadProcessMemoryProc64 callback function","_win32_readprocessmemoryproc64","base.readprocessmemoryproc64","dbghelp/ReadProcessMemoryProc64"]
old-location: base\readprocessmemoryproc64.htm
tech.root: Debug
ms.assetid: 84ff0085-295d-48bd-baa5-d6b2845520a6
ms.date: 08/03/2022
ms.keywords: PREAD_PROCESS_MEMORY_ROUTINE, PREAD_PROCESS_MEMORY_ROUTINE64, ReadProcessMemoryProc64, ReadProcessMemoryProc64 callback, ReadProcessMemoryProc64 callback function, _win32_readprocessmemoryproc64, base.readprocessmemoryproc64, dbghelp/ReadProcessMemoryProc64
req.header: dbghelp.h
req.include-header: 
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
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - PREAD_PROCESS_MEMORY_ROUTINE64
 - dbghelp/PREAD_PROCESS_MEMORY_ROUTINE64
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - DbgHelp.h
api_name:
 - ReadProcessMemoryProc64
---

# PREAD_PROCESS_MEMORY_ROUTINE64 callback function

## -description

An application-defined callback function used with the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-stackwalk">StackWalk64</a> function. It is called when 
<b>StackWalk64</b> needs to read memory from the address space of the process.

The <b>PREAD_PROCESS_MEMORY_ROUTINE64</b> type defines a pointer to this callback function. 
<b>ReadProcessMemoryProc64</b> is a placeholder for the application-defined function name.

## -parameters

### -param hProcess [in]

A handle to the process for which the stack trace is generated.

### -param qwBaseAddress [in]

The base address of the memory to be read.

### -param lpBuffer [out]

A pointer to a buffer that receives the memory to be read.

### -param nSize [in]

The size of the memory to be read, in bytes.

### -param lpNumberOfBytesRead [out]

A pointer to a variable that receives the number of bytes actually read.

## -returns

If the function succeeds, the return value should be <b>TRUE</b>. If the function fails, the return value should be <b>FALSE</b>.

## -remarks

In many cases, this function can best service the callback with a corresponding call to <a href="/windows/desktop/api/memoryapi/nf-memoryapi-readprocessmemory">ReadProcessMemory</a>.

This function should read as much of the requested memory as possible. The 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-stackwalk">StackWalk64</a> function handles the case where only part of the requested memory is read.

This callback function supersedes the <i>PREAD_PROCESS_MEMORY_ROUTINE</i> callback function.  <i>PREAD_PROCESS_MEMORY_ROUTINE</i> is defined as follows in Dbghelp.h. 


```cpp
#if !defined(_IMAGEHLP_SOURCE_) && defined(_IMAGEHLP64)
#define PREAD_PROCESS_MEMORY_ROUTINE PREAD_PROCESS_MEMORY_ROUTINE64
#else
typedef
BOOL
(__stdcall *PREAD_PROCESS_MEMORY_ROUTINE)(
    __in HANDLE hProcess,
    __in DWORD lpBaseAddress,
    __out_bcount(nSize) PVOID lpBuffer,
    __in DWORD nSize,
    __out PDWORD lpNumberOfBytesRead
    );
#endif
```

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-readprocessmemory">ReadProcessMemory</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-stackwalk">StackWalk64</a>
