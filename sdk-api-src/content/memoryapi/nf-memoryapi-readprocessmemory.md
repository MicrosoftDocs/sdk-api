---
UID: NF:memoryapi.ReadProcessMemory
title: ReadProcessMemory function (memoryapi.h)
description: Reads data from an area of memory in a specified process. The entire area to be read must be accessible or the operation fails.
helpviewer_keywords: ["ReadProcessMemory","ReadProcessMemory function","_win32_ReadProcessMemory","base.ReadProcessMemory","memoryapi/ReadProcessMemory"]
old-location: base\ReadProcessMemory.htm
tech.root: Debug
ms.assetid: 8774e145-ee7f-44de-85db-0445b905f986
ms.date: 03/10/2020
ms.keywords: ReadProcessMemory, ReadProcessMemory function, _win32_ReadProcessMemory, base.ReadProcessMemory, memoryapi/ReadProcessMemory
req.header: memoryapi.h
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
req.lib: onecore.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ReadProcessMemory
 - memoryapi/ReadProcessMemory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-memory-l1-1-9.dll
 - api-ms-win-core-memory-l1-1-8.dll
 - api-ms-win-core-memory-l1-1-7.dll
 - api-ms-win-core-memory-l1-1-6.dll
 - api-ms-win-core-memory-l1-1-5.dll
 - Kernel32.dll
 - API-MS-Win-Core-memory-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-memory-l1-1-1.dll
 - API-MS-Win-Core-memory-l1-1-2.dll
 - API-MS-Win-Core-memory-l1-1-3.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Memory-L1-1-4.dll
api_name:
 - ReadProcessMemory
---

# ReadProcessMemory function

## Description

Reads data from an area of memory in a specified process. The entire area to be read must be accessible or the operation fails.


## -parameters

### -param hProcess [in]

A handle to the process with memory that is being read. The handle must have PROCESS_VM_READ access to the process.

### -param lpBaseAddress [in]

A pointer to the base address in the specified process from which to read. Before any data transfer occurs, the system verifies that all data in the base address and memory of the specified size is accessible for read access, and if it is not accessible the function fails.

### -param lpBuffer [out]

A pointer to a buffer that receives the contents from the address space of the specified process.

### -param nSize [in]

The number of bytes to be read from the specified process.

### -param lpNumberOfBytesRead [out]

A pointer to a variable that receives the number of bytes transferred into the specified buffer. If *lpNumberOfBytesRead* is **NULL**, the parameter is ignored.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is 0 (zero). To get extended error information, call 
[GetLastError](../errhandlingapi/nf-errhandlingapi-getlasterror.md).

The function fails if the requested read operation crosses into an area of the process that is inaccessible.

## -remarks

**ReadProcessMemory** copies the data in the specified address range from the address space of the specified process into the specified buffer of the current process. Any process that has a handle with PROCESS_VM_READ access can call the function.

The entire area to be read must be accessible, and if it is not accessible, the function fails.

## -see-also

[Debugging Functions](/windows/win32/debug/debugging-functions), [OpenProcess](../processthreadsapi/nf-processthreadsapi-openprocess.md), [Process Functions for Debugging](/windows/win32/debug/process-functions-for-debugging), [VirtualAllocEx](./nf-memoryapi-virtualallocex.md), [WriteProcessMemory](./nf-memoryapi-writeprocessmemory.md)