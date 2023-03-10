---
UID: NS:psapi._PROCESS_MEMORY_COUNTERS
title: PROCESS_MEMORY_COUNTERS (psapi.h)
description: Contains the memory statistics for a process.
helpviewer_keywords: ["*PPROCESS_MEMORY_COUNTERS","PPROCESS_MEMORY_COUNTERS","PPROCESS_MEMORY_COUNTERS structure pointer [PSAPI]","PROCESS_MEMORY_COUNTERS","PROCESS_MEMORY_COUNTERS structure [PSAPI]","_win32_process_memory_counters_str","base.process_memory_counters_str","psapi.process_memory_counters_str","psapi/PPROCESS_MEMORY_COUNTERS","psapi/PROCESS_MEMORY_COUNTERS"]
old-location: psapi\process_memory_counters_str.htm
tech.root: psapi
ms.assetid: 288b5865-28a3-478b-ad32-c710fe4f3a81
ms.date: 12/05/2018
ms.keywords: '*PPROCESS_MEMORY_COUNTERS, PPROCESS_MEMORY_COUNTERS, PPROCESS_MEMORY_COUNTERS structure pointer [PSAPI], PROCESS_MEMORY_COUNTERS, PROCESS_MEMORY_COUNTERS structure [PSAPI], _win32_process_memory_counters_str, base.process_memory_counters_str, psapi.process_memory_counters_str, psapi/PPROCESS_MEMORY_COUNTERS, psapi/PROCESS_MEMORY_COUNTERS'
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
req.typenames: PROCESS_MEMORY_COUNTERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PROCESS_MEMORY_COUNTERS
 - psapi/_PROCESS_MEMORY_COUNTERS
 - PROCESS_MEMORY_COUNTERS
 - psapi/PROCESS_MEMORY_COUNTERS
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
 - PROCESS_MEMORY_COUNTERS
---

# PROCESS_MEMORY_COUNTERS structure


## -description

Contains the memory statistics for a process.

## -struct-fields

### -field cb

The size of the structure, in bytes.

### -field PageFaultCount

The number of page faults.

### -field PeakWorkingSetSize

The peak working set size, in bytes.

### -field WorkingSetSize

The current working set size, in bytes.

### -field QuotaPeakPagedPoolUsage

The peak paged pool usage, in bytes.

### -field QuotaPagedPoolUsage

The current paged pool usage, in bytes.

### -field QuotaPeakNonPagedPoolUsage

The peak nonpaged pool usage, in bytes.

### -field QuotaNonPagedPoolUsage

The current nonpaged pool usage, in bytes.

### -field PagefileUsage

The Commit Charge value in bytes for this process. Commit Charge is the total amount of memory that the memory manager has committed for a running process.

### -field PeakPagefileUsage

The peak value in bytes of the Commit Charge during the lifetime of this process.

## -see-also

<a href="/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo">GetProcessMemoryInfo</a>



<a href="/previous-versions/windows/desktop/legacy/aa965225(v=vs.85)">Memory Performance Information</a>



<a href="/windows/desktop/psapi/process-memory-usage-information">Process Memory Usage Information</a>



<a href="/windows/desktop/psapi/working-set-information">Working Set Information</a>