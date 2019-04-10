---
UID: NS:psapi._PERFORMANCE_INFORMATION
title: PERFORMANCE_INFORMATION (psapi.h)
author: windows-sdk-content
description: Contains performance information.
old-location: psapi\performance_information_str.htm
tech.root: psapi
ms.assetid: efc47f6e-1a60-4e77-9e5d-c725f9042ab8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PPERFORMACE_INFORMATION, *PPERFORMANCE_INFORMATION, PERFORMACE_INFORMATION, PERFORMANCE_INFORMATION, PERFORMANCE_INFORMATION structure [PSAPI], PPERFORMANCE_INFORMATION, PPERFORMANCE_INFORMATION structure pointer [PSAPI], _win32_performance_information_str, base.performance_information_str, psapi.performance_information_str, psapi/PERFORMANCE_INFORMATION, psapi/PPERFORMANCE_INFORMATION"
ms.topic: struct
req.header: psapi.h
req.include-header: 
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
 - Psapi.h
api_name:
 - PERFORMANCE_INFORMATION
product: Windows
targetos: Windows
req.typenames: PERFORMANCE_INFORMATION, *PPERFORMANCE_INFORMATION, PERFORMACE_INFORMATION, *PPERFORMACE_INFORMATION
req.redist: 
---

# PERFORMANCE_INFORMATION structure


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
 

 

