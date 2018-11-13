---
UID: NF:memoryapi.VirtualQuery
title: VirtualQuery function
author: windows-sdk-content
description: Retrieves information about a range of pages in the virtual address space of the calling process.
old-location: base\virtualquery.htm
tech.root: Memory
ms.assetid: 3b1f7d27-1f5d-452e-b58f-560cd9b9cbd3
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: VirtualQuery, VirtualQuery function, _win32_virtualquery, base.virtualquery, winbase/VirtualQuery
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: memoryapi.h
req.include-header: Windows.h, Memoryapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - VirtualQuery
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# VirtualQuery function


## -description


Retrieves information about a range of pages in the virtual address space of the calling process.

To retrieve information about a range of pages in the address space of another process, use the 
<a href="https://msdn.microsoft.com/19e1d875-f661-47cd-bba7-4327a2bbfacc">VirtualQueryEx</a> function.


## -parameters




### -param lpAddress [in, optional]

A pointer to the base address of the region of pages to be queried. This value is rounded down to the next page boundary. To determine the size of a page on the host computer, use the 
<a href="https://msdn.microsoft.com/f6d745af-729a-494e-90b4-19fe7d97c7af">GetSystemInfo</a> function.

If <i>lpAddress</i> specifies an address above the highest memory address accessible to the process, the function fails with <b>ERROR_INVALID_PARAMETER</b>.


### -param lpBuffer [out]

A pointer to a 
<a href="https://msdn.microsoft.com/dc3fa48e-0986-49cc-88a9-ff8179fbe5f0">MEMORY_BASIC_INFORMATION</a> structure in which information about the specified page range is returned.


### -param dwLength [in]

The size of the buffer pointed to by the <i>lpBuffer</i> parameter, in bytes.


## -returns



The return value is the actual number of bytes returned in the information buffer.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Possible error values include <b>ERROR_INVALID_PARAMETER</b>.




## -remarks



<b>VirtualQuery</b> provides information about a region of consecutive pages beginning at a specified address that share the following attributes:

<ul>
<li>The state of all pages is the same (<b>MEM_COMMIT</b>, <b>MEM_RESERVE</b>, <b>MEM_FREE</b>, <b>MEM_PRIVATE</b>, <b>MEM_MAPPED</b>, or <b>MEM_IMAGE</b>).</li>
<li>If the initial page is not free, all pages in the region are part of the same initial allocation of pages created by a single call to <a href="https://msdn.microsoft.com/a720dd89-c47c-4e48-bbc6-f2e02dfc4ed2">VirtualAlloc</a>, <a href="https://msdn.microsoft.com/df9f54cd-b2de-4107-a1c5-d5a07045851e">MapViewOfFile</a>, or one of the following extended versions of these functions: <a href="https://msdn.microsoft.com/ff0b6b79-40f5-499c-b797-b66797654164">VirtualAllocEx</a>, <a href="https://msdn.microsoft.com/dcafd557-834e-4fdf-9cb2-aad76109ad92">VirtualAllocExNuma</a>, <a href="https://msdn.microsoft.com/2ac8a7d6-5c52-41de-acb9-d7f975fd2a94">MapViewOfFileEx</a>, <a href="https://msdn.microsoft.com/1e28c8db-112d-481d-b470-8ca618e125ce">MapViewOfFileExNuma</a>.</li>
<li>The access granted to all pages is the same (<b>PAGE_READONLY</b>, <b>PAGE_READWRITE</b>, <b>PAGE_NOACCESS</b>, <b>PAGE_WRITECOPY</b>, <b>PAGE_EXECUTE</b>, <b>PAGE_EXECUTE_READ</b>, <b>PAGE_EXECUTE_READWRITE</b>, <b>PAGE_EXECUTE_WRITECOPY</b>, <b>PAGE_GUARD</b>, or <b>PAGE_NOCACHE</b>).</li>
</ul>
The function determines the attributes of the first page in the region and then scans subsequent pages until it scans the entire range of pages or until it encounters a page with a nonmatching set of attributes. The function returns the attributes and the size of the region of pages with matching attributes, in bytes. For example, if there is a 40 megabyte (MB) region of free memory, and 
<b>VirtualQuery</b> is called on a page that is 10 MB into the region, the function will obtain a state of <b>MEM_FREE</b> and a size of 30 MB.

If a shared copy-on-write page is modified, it becomes private to the process that modified the page. However, the <b>VirtualQuery</b> function will continue to report such pages as <b>MEM_MAPPED</b> (for data views) or <b>MEM_IMAGE</b> (for executable image views) rather than <b>MEM_PRIVATE</b>. To detect whether copy-on-write has occurred for a specific page, either access the page or lock it using the <a href="https://msdn.microsoft.com/414c4704-36f2-40f9-a69a-9d53ab354c30">VirtualLock</a> function to make sure the page is resident in memory, then use the <a href="https://msdn.microsoft.com/59ae76c9-e954-4648-9c9f-787136375b02">QueryWorkingSetEx</a> function to check the <b>Shared</b> bit in the extended working set information for the page. If the <b>Shared</b> bit is clear, the page is private.

This function reports on a region of pages in the memory of the calling process, and the 
<a href="https://msdn.microsoft.com/19e1d875-f661-47cd-bba7-4327a2bbfacc">VirtualQueryEx</a> function reports on a region of pages in the memory of a specified process.




## -see-also




<a href="https://msdn.microsoft.com/f6d745af-729a-494e-90b4-19fe7d97c7af">GetSystemInfo</a>



<a href="https://msdn.microsoft.com/dc3fa48e-0986-49cc-88a9-ff8179fbe5f0">MEMORY_BASIC_INFORMATION</a>



<a href="https://msdn.microsoft.com/df9f54cd-b2de-4107-a1c5-d5a07045851e">MapViewOfFile</a>



<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">Memory
    Management Functions</a>



<a href="https://msdn.microsoft.com/9488a854-1ef0-488f-b3d1-57c1acb82a88">Virtual Memory Functions</a>



<a href="https://msdn.microsoft.com/19e1d875-f661-47cd-bba7-4327a2bbfacc">VirtualQueryEx</a>
 

 

