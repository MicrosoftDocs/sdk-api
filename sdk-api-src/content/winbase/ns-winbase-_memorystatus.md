---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _MEMORYSTATUS structure


## -description


Contains information about the current state of both physical and virtual memory. The 
<a href="https://msdn.microsoft.com/473e4172-b57a-4fc6-9bb2-e916ac3c9a2f">GlobalMemoryStatus</a> function stores information in a 
<b>MEMORYSTATUS</b> structure.


## -struct-fields




### -field dwLength

The size of the 
<b>MEMORYSTATUS</b> data structure, in bytes. You do not need to set this member before calling the 
<a href="https://msdn.microsoft.com/473e4172-b57a-4fc6-9bb2-e916ac3c9a2f">GlobalMemoryStatus</a> function; the function sets it.


### -field dwMemoryLoad

A number between 0 and 100 that specifies the approximate percentage of physical memory that is in use (0 indicates no memory use and 100 indicates full memory use). 



					


### -field dwTotalPhys

The amount of actual physical memory, in bytes.


### -field dwAvailPhys

The amount of physical memory currently available, in bytes. This is the amount of physical memory that can be immediately reused without having to write its contents to disk first. It is the sum of the size of the standby, free, and zero lists.


### -field dwTotalPageFile

The current size of the committed memory limit, in bytes. This is physical memory plus the size of the page file, minus a small overhead.


### -field dwAvailPageFile

The maximum amount of memory the current process can commit, in bytes. This value should be smaller than the system-wide available commit. To calculate this value, call <a href="https://msdn.microsoft.com/21655278-49da-4e63-a4f9-0ee9f6179f4a">GetPerformanceInfo</a> and subtract the value of <b>CommitTotal</b> from <b>CommitLimit</b>.


### -field dwTotalVirtual

The size of the user-mode portion of the virtual address space of the calling process, in bytes. This value depends on the type of process, the type of processor, and the configuration of the operating system. For example, this value is approximately 2 GB for most 32-bit processes on an x86 processor and approximately 3 GB for 32-bit processes that are large address aware running on a system with 4 GT RAM Tuning enabled.


### -field dwAvailVirtual

The amount of unreserved and uncommitted memory currently in the user-mode portion of the virtual address space of the calling process, in bytes.


## -remarks



<b>MEMORYSTATUS</b> reflects the state of memory at the time of the call. It also reflects the size of the paging file at that time. The operating system can enlarge the paging file up to the maximum size set by the administrator.

On computers with more than 4 GB of memory, the 
<b>MEMORYSTATUS</b> structure can return incorrect information, reporting a value of –1 to indicate an overflow. If your application is at risk for this behavior, use the 
<a href="https://msdn.microsoft.com/bdcee13f-85be-4b9d-b108-3c5ea616dfbb">GlobalMemoryStatusEx</a> function instead of the 
<a href="https://msdn.microsoft.com/473e4172-b57a-4fc6-9bb2-e916ac3c9a2f">GlobalMemoryStatus</a> function.


#### Examples

For an example, see the 
<a href="https://msdn.microsoft.com/473e4172-b57a-4fc6-9bb2-e916ac3c9a2f">GlobalMemoryStatus</a> function.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/473e4172-b57a-4fc6-9bb2-e916ac3c9a2f">GlobalMemoryStatus</a>



<a href="https://msdn.microsoft.com/bdcee13f-85be-4b9d-b108-3c5ea616dfbb">GlobalMemoryStatusEx</a>



<a href="https://msdn.microsoft.com/b27ca747-8fd2-4267-9979-4e2e14a5a19f">Memory Performance Information</a>
 

 

