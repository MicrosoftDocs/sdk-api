---
UID: NF:memoryapi.VirtualProtectEx
title: VirtualProtectEx function
author: windows-sdk-content
description: Changes the protection on a region of committed pages in the virtual address space of a specified process.
old-location: base\virtualprotectex.htm
tech.root: memory
ms.assetid: 6afd7ae6-e4c5-483c-a638-c85781674c7b
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: VirtualProtectEx, VirtualProtectEx function, _win32_virtualprotectex, base.virtualprotectex, winbase/VirtualProtectEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: memoryapi.h
req.include-header: Windows.h, Memoryapi.h
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
 - VirtualProtectEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# VirtualProtectEx function


## -description


Changes the protection on a region of committed pages in the virtual address space of a specified 
    process.


## -parameters




### -param hProcess [in]

A handle to the process whose memory protection is to be changed. The handle must have the 
      <b>PROCESS_VM_OPERATION</b> access right. For more information, see 
      <a href="https://msdn.microsoft.com/508a17c4-88cd-431a-a102-00180a7f7ab5">Process Security and Access Rights</a>.


### -param lpAddress [in]

A pointer to the base address of the region of pages whose access protection attributes are to be changed.

All pages in the specified region must be within the same reserved region allocated when calling the 
       <a href="https://msdn.microsoft.com/a720dd89-c47c-4e48-bbc6-f2e02dfc4ed2">VirtualAlloc</a> or 
       <a href="https://msdn.microsoft.com/ff0b6b79-40f5-499c-b797-b66797654164">VirtualAllocEx</a> function using 
       <b>MEM_RESERVE</b>. The pages cannot span adjacent reserved regions that were allocated by 
       separate calls to <b>VirtualAlloc</b> or 
       <b>VirtualAllocEx</b> using 
       <b>MEM_RESERVE</b>.


### -param dwSize [in]

The size of the region whose access protection attributes are changed, in bytes. The region of affected 
     pages includes all pages containing one or more bytes in the range from the <i>lpAddress</i> 
     parameter to <code>(lpAddress+dwSize)</code>. This means that a 2-byte 
     range straddling a page boundary causes the protection attributes of both pages to be changed.


### -param flNewProtect [in]

The memory protection option. This parameter can be one of the 
       <a href="https://msdn.microsoft.com/09839db7-2118-4a7d-a707-a08c92bd600c">memory protection constants</a>.

For mapped views, this value must be compatible with the access protection specified when the view was 
       mapped (see <a href="https://msdn.microsoft.com/df9f54cd-b2de-4107-a1c5-d5a07045851e">MapViewOfFile</a>, 
       <a href="https://msdn.microsoft.com/2ac8a7d6-5c52-41de-acb9-d7f975fd2a94">MapViewOfFileEx</a>, and 
       <a href="https://msdn.microsoft.com/1e28c8db-112d-481d-b470-8ca618e125ce">MapViewOfFileExNuma</a>).


### -param lpflOldProtect [out]

A pointer to a variable that receives the previous access protection of the first page in the specified 
      region of pages. If this parameter is <b>NULL</b> or does not point to a valid variable, the 
      function fails.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The access protection value can be set only on committed pages. If the state of any page in the specified 
    region is not committed, the function fails and returns without modifying the access protection of any pages in 
    the specified region.

The <b>PAGE_GUARD</b> protection modifier establishes guard pages. Guard pages act as 
    one-shot access alarms. For more information, see 
    <a href="https://msdn.microsoft.com/763bc763-e178-481e-a81a-c15715e56901">Creating Guard Pages</a>.

It is best to avoid using <b>VirtualProtectEx</b> to 
    change page protections on memory blocks allocated by 
    <a href="https://msdn.microsoft.com/06886545-bd5c-4d81-b1c3-dfa7e146e43a">GlobalAlloc</a>, 
    <a href="https://msdn.microsoft.com/9a176312-0312-4cc1-baf5-949b346d983e">HeapAlloc</a>, or 
    <a href="https://msdn.microsoft.com/da8cd2be-ff4c-4da5-813c-8759a58228c9">LocalAlloc</a>, because multiple memory blocks can exist on a 
    single page. The heap manager assumes that all pages in the heap grant at least read and write access.

When protecting a region that will be executable, the calling program bears responsibility for ensuring cache 
    coherency via an appropriate call to 
    <a href="https://msdn.microsoft.com/6267adde-8169-4673-97ec-78c66e2135c1">FlushInstructionCache</a> once the code has been set 
    in place. Otherwise attempts to execute code out of the newly executable region may produce unpredictable 
    results.




## -see-also




<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">Memory Management Functions</a>



<a href="https://msdn.microsoft.com/9488a854-1ef0-488f-b3d1-57c1acb82a88">Virtual Memory Functions</a>



<a href="https://msdn.microsoft.com/a720dd89-c47c-4e48-bbc6-f2e02dfc4ed2">VirtualAlloc</a>



<a href="https://msdn.microsoft.com/a0018bba-226b-4c18-8ea4-15e69524db11">VirtualProtect</a>



<a href="https://msdn.microsoft.com/19e1d875-f661-47cd-bba7-4327a2bbfacc">VirtualQueryEx</a>
 

 

