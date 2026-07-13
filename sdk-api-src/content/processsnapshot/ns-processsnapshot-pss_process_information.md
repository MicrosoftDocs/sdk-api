---
UID: NS:processsnapshot.PSS_PROCESS_INFORMATION
title: PSS_PROCESS_INFORMATION (processsnapshot.h)
description: Holds process information returned by PssQuerySnapshot.
helpviewer_keywords: ["PSS_PROCESS_INFORMATION","PSS_PROCESS_INFORMATION structure","proc_snap.pss_process_information","processsnapshot/PSS_PROCESS_INFORMATION"]
old-location: proc_snap\pss_process_information.htm
tech.root: proc_snap
ms.assetid: D629FA42-B501-4A0E-9B53-6D70E580B687
ms.date: 12/05/2018
ms.keywords: PSS_PROCESS_INFORMATION, PSS_PROCESS_INFORMATION structure, proc_snap.pss_process_information, processsnapshot/PSS_PROCESS_INFORMATION
req.header: processsnapshot.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
req.typenames: PSS_PROCESS_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PSS_PROCESS_INFORMATION
 - processsnapshot/PSS_PROCESS_INFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - processsnapshot.h
api_name:
 - PSS_PROCESS_INFORMATION
---

# PSS_PROCESS_INFORMATION structure


## -description

Holds process information returned by <a href="/previous-versions/windows/desktop/api/processsnapshot/nf-processsnapshot-pssquerysnapshot">PssQuerySnapshot</a>.

## -struct-fields

### -field ExitStatus

The exit code of the process. If the process has not exited, this is set to <b>STILL_ACTIVE</b> (259).

### -field PebBaseAddress

The address to the process environment block (PEB). Reserved for use by the operating system.

### -field AffinityMask

The affinity mask of the process.

### -field BasePriority

The base priority level of the process.

### -field ProcessId

The process ID.

### -field ParentProcessId

The parent process ID.

### -field Flags

Flags about the process. For more information, see <a href="/previous-versions/windows/desktop/api/processsnapshot/ne-processsnapshot-pss_process_flags">PSS_PROCESS_FLAGS</a>.

### -field CreateTime

The time the process was created. For more information, see <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>.

### -field ExitTime

If the process exited, the time of the exit. For more information, see <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>.

### -field KernelTime

The amount of time the process spent executing in kernel-mode. For more information, see <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>.

### -field UserTime

The amount of time the process spent executing in user-mode. For more information, see <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>.

### -field PriorityClass

The priority class.

### -field PeakVirtualSize

A memory usage counter. See the <a href="/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo">GetProcessMemoryInfo</a> function for more information.

### -field VirtualSize

A memory usage counter. See the <a href="/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo">GetProcessMemoryInfo</a> function for more information.

### -field PageFaultCount

A memory usage counter. See the <a href="/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo">GetProcessMemoryInfo</a> function for more information.

### -field PeakWorkingSetSize

A memory usage counter. See the <a href="/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo">GetProcessMemoryInfo</a> function for more information.

### -field WorkingSetSize

A memory usage counter. See the <a href="/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo">GetProcessMemoryInfo</a> function for more information.

### -field QuotaPeakPagedPoolUsage

A memory usage counter. See the <a href="/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo">GetProcessMemoryInfo</a> function for more information.

### -field QuotaPagedPoolUsage

A memory usage counter. See the <a href="/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo">GetProcessMemoryInfo</a> function for more information.

### -field QuotaPeakNonPagedPoolUsage

A memory usage counter. See the <a href="/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo">GetProcessMemoryInfo</a> function for more information.

### -field QuotaNonPagedPoolUsage

A memory usage counter. See the <a href="/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo">GetProcessMemoryInfo</a> function for more information.

### -field PagefileUsage

A memory usage counter. See the <a href="/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo">GetProcessMemoryInfo</a> function for more information.

### -field PeakPagefileUsage

A memory usage counter. See the <a href="/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo">GetProcessMemoryInfo</a> function for more information.

### -field PrivateUsage

A memory usage counter. See the <a href="/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo">GetProcessMemoryInfo</a> function for more information.

### -field ExecuteFlags

Reserved for use by the operating system.

### -field ImageFileName

The full path to the process executable. If the path exceeds the allocated buffer size, it is truncated.

## -remarks

<a href="/previous-versions/windows/desktop/api/processsnapshot/nf-processsnapshot-pssquerysnapshot">PssQuerySnapshot</a> returns a <b>PSS_PROCESS_INFORMATION</b> structure when the <a href="/previous-versions/windows/desktop/api/processsnapshot/ne-processsnapshot-pss_query_information_class">PSS_QUERY_INFORMATION_CLASS</a> member that the caller provides it is  <b>PSS_QUERY_PROCESS_INFORMATION</b>.

## -see-also

<a href="/previous-versions/windows/desktop/proc_snap/process-snapshotting-portal">Process Snapshotting</a>

