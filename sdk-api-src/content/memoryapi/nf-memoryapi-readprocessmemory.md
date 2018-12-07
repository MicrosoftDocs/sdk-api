---
UID: NF:memoryapi.ReadProcessMemory
title: ReadProcessMemory function
author: windows-sdk-content
description: Reads data from an area of memory in a specified process. The entire area to be read must be accessible or the operation fails.
old-location: base\readprocessmemory.htm
tech.root: debug
ms.assetid: 8774e145-ee7f-44de-85db-0445b905f986
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ReadProcessMemory, ReadProcessMemory function, _win32_readprocessmemory, base.readprocessmemory, memoryapi/ReadProcessMemory
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ReadProcessMemory function


## -description


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

A pointer to a variable that receives the number of bytes transferred into the specified buffer. If <i>lpNumberOfBytesRead</i> is <b>NULL</b>, the parameter is ignored.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is 0 (zero). To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The function fails if the requested read operation crosses into an area of the process that is inaccessible.




## -remarks



<b>ReadProcessMemory</b> copies the data in the specified address range from the address space of the specified process into the specified buffer of the current process. Any process that has a handle with PROCESS_VM_READ access can call the function.

The entire area to be read must be accessible, and if it is not accessible, the function fails.




## -see-also




<a href="https://msdn.microsoft.com/95a838a2-f138-4682-b733-3f363b6c4a4b">Debugging Functions</a>



<a href="https://msdn.microsoft.com/8f695c38-19c4-49e4-97de-8b64ea536cb1">OpenProcess</a>



<a href="https://msdn.microsoft.com/7056e181-9bc5-4530-a7b8-d5ff1e345eef">Process Functions for Debugging</a>



<a href="https://msdn.microsoft.com/ff0b6b79-40f5-499c-b797-b66797654164">VirtualAllocEx</a>



<a href="https://msdn.microsoft.com/9cd91f1c-58ce-4adc-b027-45748543eb06">WriteProcessMemory</a>
 

 

