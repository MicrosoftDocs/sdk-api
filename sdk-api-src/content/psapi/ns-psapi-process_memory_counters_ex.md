---
UID: NS:psapi._PROCESS_MEMORY_COUNTERS_EX
title: PROCESS_MEMORY_COUNTERS_EX (psapi.h)
description: Contains extended memory statistics for a process.
helpviewer_keywords: ["*PPROCESS_MEMORY_COUNTERS_EX","PPROCESS_MEMORY_COUNTERS_EX","PPROCESS_MEMORY_COUNTERS_EX structure pointer [PSAPI]","PROCESS_MEMORY_COUNTERS_EX","PROCESS_MEMORY_COUNTERS_EX structure [PSAPI]","_win32_process_memory_counters_ex","base.process_memory_counters_ex","psapi.process_memory_counters_ex","psapi/PPROCESS_MEMORY_COUNTERS_EX","psapi/PROCESS_MEMORY_COUNTERS_EX"]
old-location: psapi\process_memory_counters_ex.htm
tech.root: psapi
ms.assetid: cf06445d-b71a-4320-afc8-4bd88ebfb284
ms.date: 12/05/2018
ms.keywords: '*PPROCESS_MEMORY_COUNTERS_EX, PPROCESS_MEMORY_COUNTERS_EX, PPROCESS_MEMORY_COUNTERS_EX structure pointer [PSAPI], PROCESS_MEMORY_COUNTERS_EX, PROCESS_MEMORY_COUNTERS_EX structure [PSAPI], _win32_process_memory_counters_ex, base.process_memory_counters_ex, psapi.process_memory_counters_ex, psapi/PPROCESS_MEMORY_COUNTERS_EX, psapi/PROCESS_MEMORY_COUNTERS_EX'
req.header: psapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
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
req.typenames: PROCESS_MEMORY_COUNTERS_EX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PROCESS_MEMORY_COUNTERS_EX
 - psapi/_PROCESS_MEMORY_COUNTERS_EX
 - PROCESS_MEMORY_COUNTERS_EX
 - psapi/PROCESS_MEMORY_COUNTERS_EX
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
 - PROCESS_MEMORY_COUNTERS_EX
---

# PROCESS_MEMORY_COUNTERS_EX structure


## -description

Contains extended memory statistics for a process.

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

The Commit Charge value in bytes for this process. Commit Charge is the total amount of private memory that the memory manager has committed for a running process.

<b>Windows 7 and Windows Server 2008 R2 and earlier:  </b><b>PagefileUsage</b> is always zero. Check <b>PrivateUsage</b> instead.

### -field PeakPagefileUsage

The peak value in bytes of the Commit Charge during the lifetime of this process.

### -field PrivateUsage

Same as <b>PagefileUsage</b>. The Commit Charge value in bytes for this process. Commit Charge is the total amount of private memory that the memory manager has committed for a running process.

## -see-also

<a href="/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo">GetProcessMemoryInfo</a>



<a href="/previous-versions/windows/desktop/legacy/aa965225(v=vs.85)">Memory Performance Information</a>



<a href="/windows/desktop/psapi/process-memory-usage-information">Process Memory Usage Information</a>



<a href="/windows/desktop/psapi/working-set-information">Working Set Information</a>