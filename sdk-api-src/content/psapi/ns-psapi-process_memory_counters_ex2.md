---
UID: NS:psapi._PROCESS_MEMORY_COUNTERS_EX2
tech.root: psapi
title: PROCESS_MEMORY_COUNTERS_EX2
ms.date: 01/05/2024
targetos: Windows
description: Contains extended memory statistics for a process. Extends PROCESS_MEMORY_COUNTERS_EX.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: psapi.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10 22H2 with September 2023 cumulative update or Windows 11 22H2 with September 2023 cumulative update
req.target-min-winversvr: 
req.target-type: 
req.typenames: PROCESS_MEMORY_COUNTERS_EX2
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - psapi.h
api_name:
 - _PROCESS_MEMORY_COUNTERS_EX2
 - PROCESS_MEMORY_COUNTERS_EX2
f1_keywords:
 - _PROCESS_MEMORY_COUNTERS_EX2
 - psapi/_PROCESS_MEMORY_COUNTERS_EX2
 - PROCESS_MEMORY_COUNTERS_EX2
 - psapi/PROCESS_MEMORY_COUNTERS_EX2
dev_langs:
 - c++
helpviewer_keywords:
 - _PROCESS_MEMORY_COUNTERS_EX2
---

## -description

Contains extended memory statistics for a process. Extends PROCESS_MEMORY_COUNTERS_EX.

## -struct-fields

### -field cb

The size of the structure, in bytes.

### -field PageFaultCount

The number of page faults.

### -field PeakWorkingSetSize

The peak working set size, in bytes.

### -field WorkingSetSize

The current working set size, in bytes

### -field QuotaPeakPagedPoolUsage

The peak paged pool usage, in bytes.

### -field QuotaPagedPoolUsage

The current paged pool usage, in bytes.

### -field QuotaPeakNonPagedPoolUsage

The peak non-paged pool usage, in bytes.

### -field QuotaNonPagedPoolUsage

The current non-paged pool usage, in bytes.

### -field PagefileUsage

The Commit Charge value in bytes for this process. Commit Charge is the total amount of private memory that the memory manager has committed for a running process.

### -field PeakPagefileUsage

The peak value in bytes of the Commit Charge during the lifetime of this process.

### -field PrivateUsage

Same as **PagefileUsage**. The Commit Charge value in bytes for this process. Commit Charge is the total amount of private memory that the memory manager has committed for a running process.

### -field PrivateWorkingSetSize

The current private working set size, in bytes.

### -field SharedCommitUsage

The current shared commit usage, in bytes.

## -remarks

## -see-also

[PROCESS_MEMORY_COUNTERS_EX](ns-psapi-process_memory_counters_ex.md)
