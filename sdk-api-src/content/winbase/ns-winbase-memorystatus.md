---
UID: NS:winbase._MEMORYSTATUS
title: MEMORYSTATUS (winbase.h)
description: Contains information about the current state of both physical and virtual memory.
helpviewer_keywords: ["*LPMEMORYSTATUS","LPMEMORYSTATUS","LPMEMORYSTATUS structure pointer","MEMORYSTATUS","MEMORYSTATUS structure","_MEMORYSTATUS","_win32_memorystatus_str","base.memorystatus_str","winbase/LPMEMORYSTATUS","winbase/_MEMORYSTATUS"]
old-location: base\memorystatus_str.htm
tech.root: base
ms.assetid: 7815ec8f-cacf-4c1b-b5f7-5bb3ef8d759c
ms.date: 12/05/2018
ms.keywords: '*LPMEMORYSTATUS, LPMEMORYSTATUS, LPMEMORYSTATUS structure pointer, MEMORYSTATUS, MEMORYSTATUS structure, _MEMORYSTATUS, _win32_memorystatus_str, base.memorystatus_str, winbase/LPMEMORYSTATUS, winbase/_MEMORYSTATUS'
req.header: winbase.h
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
targetos: Windows
req.typenames: MEMORYSTATUS, *LPMEMORYSTATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MEMORYSTATUS
 - winbase/_MEMORYSTATUS
 - LPMEMORYSTATUS
 - winbase/LPMEMORYSTATUS
 - MEMORYSTATUS
 - winbase/MEMORYSTATUS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
api_name:
 - MEMORYSTATUS
---

# MEMORYSTATUS structure


## -description

Contains information about the current state of both physical and virtual memory. The 
<a href="/windows/desktop/api/winbase/nf-winbase-globalmemorystatus">GlobalMemoryStatus</a> function stores information in a 
<b>MEMORYSTATUS</b> structure.

## -struct-fields

### -field dwLength

The size of the 
<b>MEMORYSTATUS</b> data structure, in bytes. You do not need to set this member before calling the 
<a href="/windows/desktop/api/winbase/nf-winbase-globalmemorystatus">GlobalMemoryStatus</a> function; the function sets it.

### -field dwMemoryLoad

A number between 0 and 100 that specifies the approximate percentage of physical memory that is in use (0 indicates no memory use and 100 indicates full memory use).

### -field dwTotalPhys

The amount of actual physical memory, in bytes.

### -field dwAvailPhys

The amount of physical memory currently available, in bytes. This is the amount of physical memory that can be immediately reused without having to write its contents to disk first. It is the sum of the size of the standby, free, and zero lists.

### -field dwTotalPageFile

The current size of the committed memory limit, in bytes. This is physical memory plus the size of the page file, minus a small overhead.

### -field dwAvailPageFile

The maximum amount of memory the current process can commit, in bytes. This value should be smaller than the system-wide available commit. To calculate this value, call <a href="/windows/desktop/api/psapi/nf-psapi-getperformanceinfo">GetPerformanceInfo</a> and subtract the value of <b>CommitTotal</b> from <b>CommitLimit</b>.

### -field dwTotalVirtual

The size of the user-mode portion of the virtual address space of the calling process, in bytes. This value depends on the type of process, the type of processor, and the configuration of the operating system. For example, this value is approximately 2 GB for most 32-bit processes on an x86 processor and approximately 3 GB for 32-bit processes that are large address aware running on a system with 4 GT RAM Tuning enabled.

### -field dwAvailVirtual

The amount of unreserved and uncommitted memory currently in the user-mode portion of the virtual address space of the calling process, in bytes.

## -remarks

<b>MEMORYSTATUS</b> reflects the state of memory at the time of the call. It also reflects the size of the paging file at that time. The operating system can enlarge the paging file up to the maximum size set by the administrator.

On computers with more than 4 GB of memory, the 
<b>MEMORYSTATUS</b> structure can return incorrect information, reporting a value of –1 to indicate an overflow. If your application is at risk for this behavior, use the 
<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex">GlobalMemoryStatusEx</a> function instead of the 
<a href="/windows/desktop/api/winbase/nf-winbase-globalmemorystatus">GlobalMemoryStatus</a> function.


#### Examples

For an example, see the 
<a href="/windows/desktop/api/winbase/nf-winbase-globalmemorystatus">GlobalMemoryStatus</a> function.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-globalmemorystatus">GlobalMemoryStatus</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex">GlobalMemoryStatusEx</a>



<a href="/previous-versions/windows/desktop/legacy/aa965225(v=vs.85)">Memory Performance Information</a>