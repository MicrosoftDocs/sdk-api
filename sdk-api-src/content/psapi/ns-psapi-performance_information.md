---
UID: NS:psapi._PERFORMANCE_INFORMATION
title: PERFORMANCE_INFORMATION (psapi.h)
description: Contains performance information. (PERFORMANCE_INFORMATION)
helpviewer_keywords: ["*PPERFORMACE_INFORMATION","*PPERFORMANCE_INFORMATION","PERFORMACE_INFORMATION","PERFORMANCE_INFORMATION","PERFORMANCE_INFORMATION structure [PSAPI]","PPERFORMANCE_INFORMATION","PPERFORMANCE_INFORMATION structure pointer [PSAPI]","_win32_performance_information_str","base.performance_information_str","psapi.performance_information_str","psapi/PERFORMANCE_INFORMATION","psapi/PPERFORMANCE_INFORMATION"]
old-location: psapi\performance_information_str.htm
tech.root: psapi
ms.assetid: efc47f6e-1a60-4e77-9e5d-c725f9042ab8
ms.date: 12/05/2018
ms.keywords: '*PPERFORMACE_INFORMATION, *PPERFORMANCE_INFORMATION, PERFORMACE_INFORMATION, PERFORMANCE_INFORMATION, PERFORMANCE_INFORMATION structure [PSAPI], PPERFORMANCE_INFORMATION, PPERFORMANCE_INFORMATION structure pointer [PSAPI], _win32_performance_information_str, base.performance_information_str, psapi.performance_information_str, psapi/PERFORMANCE_INFORMATION, psapi/PPERFORMANCE_INFORMATION'
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
targetos: Windows
req.typenames: PERFORMANCE_INFORMATION, *PPERFORMANCE_INFORMATION, PERFORMACE_INFORMATION, *PPERFORMACE_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PERFORMANCE_INFORMATION
 - psapi/_PERFORMANCE_INFORMATION
 - PPERFORMANCE_INFORMATION
 - psapi/PPERFORMANCE_INFORMATION
 - PERFORMANCE_INFORMATION
 - psapi/PERFORMANCE_INFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Psapi.h
api_name:
 - PERFORMANCE_INFORMATION
---

# PERFORMANCE_INFORMATION structure


## -description

Contains performance information.

## -struct-fields

### -field cb

The size of this structure, in bytes.

### -field CommitTotal

The number of pages currently committed by the system. Note that committing pages (using <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc">VirtualAlloc</a> with MEM_COMMIT) changes this value immediately; however, the physical memory is not charged until the pages are accessed.

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

<a href="/windows/desktop/api/psapi/nf-psapi-getperformanceinfo">GetPerformanceInfo</a>



<a href="/previous-versions/windows/desktop/legacy/aa965225(v=vs.85)">Memory Performance Information</a>
