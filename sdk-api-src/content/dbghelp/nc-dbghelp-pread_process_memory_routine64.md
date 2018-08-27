---
UID: NC:dbghelp.PREAD_PROCESS_MEMORY_ROUTINE64
title: PREAD_PROCESS_MEMORY_ROUTINE64
author: windows-sdk-content
description: An application-defined callback function used with the StackWalk64 function. It is called when StackWalk64 needs to read memory from the address space of the process.
old-location: base\readprocessmemoryproc64.htm
old-project: debug
ms.assetid: 84ff0085-295d-48bd-baa5-d6b2845520a6
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: PREAD_PROCESS_MEMORY_ROUTINE, PREAD_PROCESS_MEMORY_ROUTINE64, ReadProcessMemoryProc64, ReadProcessMemoryProc64 callback, ReadProcessMemoryProc64 callback function, _win32_readprocessmemoryproc64, base.readprocessmemoryproc64, dbghelp/ReadProcessMemoryProc64
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: dbghelp.h
req.include-header: 
req.redist: DbgHelp.dll 5.1 or later
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
req.typenames: DAV_CALLBACK_CRED, *PDAV_CALLBACK_CRED
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - DbgHelp.h
api_name:
 - ReadProcessMemoryProc64
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PREAD_PROCESS_MEMORY_ROUTINE64 callback function


## -description


An application-defined callback function used with the 
<a href="https://msdn.microsoft.com/e2bdaa4c-5474-41a0-bcea-927570c8402c">StackWalk64</a> function. It is called when 
<b>StackWalk64</b> needs to read memory from the address space of the process.

The <b>PREAD_PROCESS_MEMORY_ROUTINE64</b> type defines a pointer to this callback function. 
<b>ReadProcessMemoryProc64</b> is a placeholder for the application-defined function name.


## -parameters




### -param hProcess [in]

A handle to the process for which the stack trace is generated.


### -param qwBaseAddress


### -param lpBuffer [out]

A pointer to a buffer that receives the memory to be read.


### -param nSize [in]

The size of the memory to be read, in bytes.


### -param lpNumberOfBytesRead [out]

A pointer to a variable that receives the number of bytes actually read.


#### - lpBaseAddress [in]

The base address of the memory to be read.


## -returns



If the function succeeds, the return value should be <b>TRUE</b>. If the function fails, the return value should be <b>FALSE</b>.




## -remarks



In many cases, this function can best service the callback with a corresponding call to <a href="https://msdn.microsoft.com/8774e145-ee7f-44de-85db-0445b905f986">ReadProcessMemory</a>.

This function should read as much of the requested memory as possible. The 
<a href="https://msdn.microsoft.com/e2bdaa4c-5474-41a0-bcea-927570c8402c">StackWalk64</a> function handles the case where only part of the requested memory is read.

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




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/8774e145-ee7f-44de-85db-0445b905f986">ReadProcessMemory</a>



<a href="https://msdn.microsoft.com/e2bdaa4c-5474-41a0-bcea-927570c8402c">StackWalk64</a>
 

 

