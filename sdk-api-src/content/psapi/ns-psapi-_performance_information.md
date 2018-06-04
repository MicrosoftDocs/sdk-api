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

# _PERFORMANCE_INFORMATION structure


## -description


Contains performance information.


## -struct-fields




### -field cb

The size of this structure, in bytes.


### -field CommitTotal

The number of pages currently committed by the system. Note that committing pages (using <a href="https://msdn.microsoft.com/a720dd89-c47c-4e48-bbc6-f2e02dfc4ed2">VirtualAlloc</a> with MEM_COMMIT) changes this value immediately; however, the physical memory is not charged until the pages are accessed.


### -field CommitLimit

The current maximum number of pages that can be committed by the system without extending the paging file(s). This number can change if memory is added or deleted, or if pagefiles have grown, shrunk, or been added. If the paging file can be extended, this is a soft limit.


### -field CommitPeak

The maximum number of pages that were simultaneously in the committed state since the last system reboot.


### -field PhysicalTotal

The amount of actual physical memory, in pages.


### -field PhysicalAvailable

The amount of physical memory currently available, in pages.  This is the amount of physical memory that can be immediately reused without having to write its contents to disk first. It is the sum of the size of the standby, free, and zero lists.


### -field SystemCache

The amount of system cache memory, in pages. This is the size of the standby list plus the system working set.


### -field KernelTotal

The sum of the memory currently in the paged and nonpaged kernel pools, in pages.


### -field KernelPaged

The memory currently in the paged kernel pool, in pages.


### -field KernelNonpaged

The memory currently in the nonpaged kernel pool, in pages.


### -field PageSize

The size of a page, in bytes.


### -field HandleCount

The current number of open handles.


### -field ProcessCount

The current number of processes.


### -field ThreadCount

The current number of threads.


## -see-also




<a href="https://msdn.microsoft.com/21655278-49da-4e63-a4f9-0ee9f6179f4a">GetPerformanceInfo</a>



<a href="https://msdn.microsoft.com/b27ca747-8fd2-4267-9979-4e2e14a5a19f">Memory Performance Information</a>
 

 

