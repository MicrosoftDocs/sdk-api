---
UID: NF:memoryapi.WriteProcessMemory
title: WriteProcessMemory function (memoryapi.h)
description: Writes data to an area of memory in a specified process. The entire area to be written to must be accessible or the operation fails.
helpviewer_keywords: ["WriteProcessMemory","WriteProcessMemory function","_win32_writeprocessmemory","base.writeprocessmemory","memoryapi/WriteProcessMemory"]
old-location: base\writeprocessmemory.htm
tech.root: Debug
ms.assetid: 9cd91f1c-58ce-4adc-b027-45748543eb06
ms.date: 12/05/2018
ms.keywords: WriteProcessMemory, WriteProcessMemory function, _win32_writeprocessmemory, base.writeprocessmemory, memoryapi/WriteProcessMemory
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
 - WriteProcessMemory
 - memoryapi/WriteProcessMemory
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
 - WriteProcessMemory
---

# WriteProcessMemory function


## -description

Writes data to an area of memory in a specified process. The entire area to be written to must be accessible or the operation fails.

## -parameters

### -param hProcess [in]

A handle to the process memory to be modified. The handle must have PROCESS_VM_WRITE and PROCESS_VM_OPERATION access to the process.

### -param lpBaseAddress [in]

A pointer to the base address in the specified process to which data is written. Before data transfer occurs, the system verifies that all data in the base address and memory of the specified size is accessible for write access, and if it is not accessible, the function fails.

### -param lpBuffer [in]

A pointer to the buffer that contains data to be written in  the address space of the specified process.

### -param nSize [in]

The number of bytes to be written to the specified process.

### -param lpNumberOfBytesWritten [out]

A pointer to a variable that receives the number of bytes transferred into the specified process. This parameter is optional. If <i>lpNumberOfBytesWritten</i> is <b>NULL</b>, the parameter is ignored.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is 0 (zero). To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. The function fails if the requested write operation crosses into an area of the process that is inaccessible.

## -remarks

<b>WriteProcessMemory</b> copies the data from the specified buffer in the current process to the address range of the specified process. Any process that has a handle with PROCESS_VM_WRITE and PROCESS_VM_OPERATION access to the process to be written to can call the function. Typically but not always, the process with address space that is being written to is  being debugged.

The entire area to be written to must be accessible, and if it is not accessible, the function fails.

## -see-also

<a href="/windows/desktop/Debug/debugging-functions">Debugging Functions</a>



<a href="/windows/desktop/Debug/process-functions-for-debugging">Process Functions for Debugging</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-readprocessmemory">ReadProcessMemory</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualallocex">VirtualAllocEx</a>