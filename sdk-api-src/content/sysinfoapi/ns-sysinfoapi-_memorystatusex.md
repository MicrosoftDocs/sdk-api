---
UID: NS:sysinfoapi._MEMORYSTATUSEX
title: "_MEMORYSTATUSEX"
author: windows-sdk-content
description: Contains information about the current state of both physical and virtual memory, including extended memory.
old-location: base\memorystatusex_str.htm
tech.root: Memory
ms.assetid: ce3c7993-8b91-4bca-8be8-9d81c26b9bef
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: "*LPMEMORYSTATUSEX, LPMEMORYSTATUSEX, LPMEMORYSTATUSEX structure pointer, MEMORYSTATUSEX, MEMORYSTATUSEX structure, _MEMORYSTATUSEX, _win32_memorystatusex_str, base.memorystatusex_str, sysinfoapi/LPMEMORYSTATUSEX, sysinfoapi/MEMORYSTATUSEX"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: sysinfoapi.h
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
 - sysinfoapi.h
api_name:
 - MEMORYSTATUSEX
product: Windows
targetos: Windows
req.typenames: MEMORYSTATUSEX, *LPMEMORYSTATUSEX
req.redist: 
---

# _MEMORYSTATUSEX structure


## -description


Contains information about the current state of both physical and virtual memory, including extended memory. The 
<a href="https://msdn.microsoft.com/bdcee13f-85be-4b9d-b108-3c5ea616dfbb">GlobalMemoryStatusEx</a> function stores information in this structure.


## -struct-fields




### -field dwLength

The size of the 
structure, in bytes. You must set this member before calling  
<a href="https://msdn.microsoft.com/bdcee13f-85be-4b9d-b108-3c5ea616dfbb">GlobalMemoryStatusEx</a>.


### -field dwMemoryLoad

A number between 0 and 100 that specifies the approximate percentage of physical memory that is in use (0 indicates no memory use and 100 indicates full memory use).


### -field ullTotalPhys

The amount of actual physical memory, in bytes.


### -field ullAvailPhys

The amount of physical memory currently available, in bytes. This is the amount of physical memory that can be immediately reused without having to write its contents to disk first. It is the sum of the size of the standby, free, and zero lists.


### -field ullTotalPageFile

The current committed memory limit for the system or the current process, whichever is smaller, in bytes. To get the system-wide committed memory limit, call <a href="https://msdn.microsoft.com/21655278-49da-4e63-a4f9-0ee9f6179f4a">GetPerformanceInfo</a>. 


### -field ullAvailPageFile

The maximum amount of memory the current process can commit, in bytes. This value is equal to or smaller than the system-wide available commit value. To calculate the system-wide available commit value, call <a href="https://msdn.microsoft.com/21655278-49da-4e63-a4f9-0ee9f6179f4a">GetPerformanceInfo</a> and subtract the value of <b>CommitTotal</b> from the value of <b>CommitLimit</b>.


### -field ullTotalVirtual

The size of the user-mode portion of the virtual address space of the calling process, in bytes. This value depends on the type of process, the type of processor, and the configuration of the operating system. For example, this value is approximately 2 GB for most 32-bit processes on an x86 processor and approximately 3 GB for 32-bit processes that are large address aware running on a system with <a href="https://msdn.microsoft.com/991eb86f-9e6f-4084-8b6f-f979e42104b5">4-gigabyte tuning</a> enabled.


### -field ullAvailVirtual

The amount of unreserved and uncommitted memory currently in the user-mode portion of the virtual address space of the calling process, in bytes.


### -field ullAvailExtendedVirtual

Reserved. This value is always 0.


## -remarks



<b>MEMORYSTATUSEX</b> reflects the state of memory at the time of the call. It also reflects the size of the paging file at that time. The operating system can enlarge the paging file up to the maximum size set by the administrator.

The physical memory sizes returned include the memory from all nodes. 


#### Examples

For an example, see the 
<a href="https://msdn.microsoft.com/bdcee13f-85be-4b9d-b108-3c5ea616dfbb">GlobalMemoryStatusEx</a> function.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/bdcee13f-85be-4b9d-b108-3c5ea616dfbb">GlobalMemoryStatusEx</a>



<a href="https://msdn.microsoft.com/b27ca747-8fd2-4267-9979-4e2e14a5a19f">Memory Performance Information</a>
 

 

