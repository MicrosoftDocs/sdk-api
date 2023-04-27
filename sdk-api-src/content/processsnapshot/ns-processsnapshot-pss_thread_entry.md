---
UID: NS:processsnapshot.PSS_THREAD_ENTRY
title: PSS_THREAD_ENTRY (processsnapshot.h)
description: Holds thread information returned by PssWalkSnapshotPssWalkSnapshot.
helpviewer_keywords: ["PSS_THREAD_ENTRY","PSS_THREAD_ENTRY structure","proc_snap.pss_thread_entry","processsnapshot/PSS_THREAD_ENTRY"]
old-location: proc_snap\pss_thread_entry.htm
tech.root: proc_snap
ms.assetid: 99C89DBB-8C12-482E-B33D-AE59C37662CF
ms.date: 12/05/2018
ms.keywords: PSS_THREAD_ENTRY, PSS_THREAD_ENTRY structure, proc_snap.pss_thread_entry, processsnapshot/PSS_THREAD_ENTRY
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
req.typenames: PSS_THREAD_ENTRY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PSS_THREAD_ENTRY
 - processsnapshot/PSS_THREAD_ENTRY
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
 - PSS_THREAD_ENTRY
---

# PSS_THREAD_ENTRY structure


## -description

Holds thread information  returned by <a href="/previous-versions/windows/desktop/api/processsnapshot/nf-processsnapshot-psswalksnapshot">PssWalkSnapshot</a><b>PssWalkSnapshot</b>.

## -struct-fields

### -field ExitStatus

The exit code of the process. If the process has not exited, this is set to <b>STILL_ACTIVE</b> (259).

### -field TebBaseAddress

The address of the thread environment block (TEB). Reserved for use by the operating system.

### -field ProcessId

The process ID.

### -field ThreadId

The thread ID.

### -field AffinityMask

The affinity mask of the process.

### -field Priority

The thread’s dynamic priority level.

### -field BasePriority

The base priority level of the process.

### -field LastSyscallFirstArgument

Reserved for use by the operating system.

### -field LastSyscallNumber

Reserved for use by the operating system.

### -field CreateTime

The time the thread was created. For more information, see <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>.

### -field ExitTime

If the thread exited, the time of the exit. For more information, see <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>.

### -field KernelTime

The amount of time the thread spent executing in kernel mode. For more information, see <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>.

### -field UserTime

The amount of time the thread spent executing in user mode. For more information, see <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>.

### -field Win32StartAddress

A pointer to the thread procedure for thread.

### -field CaptureTime

The capture time of this thread. For more information, see <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>.

### -field Flags

Flags about the thread. For more information, see <a href="/previous-versions/windows/desktop/api/processsnapshot/ne-processsnapshot-pss_thread_flags">PSS_THREAD_FLAGS</a>.

### -field SuspendCount

The    count of times the thread suspended.

### -field SizeOfContextRecord

The size of <i>ContextRecord</i>, in bytes.

### -field ContextRecord

A pointer to the context record if thread context information was captured. The pointer is valid for the lifetime of the walk marker passed to <a href="/previous-versions/windows/desktop/api/processsnapshot/nf-processsnapshot-psswalksnapshot">PssWalkSnapshot</a>.

## -remarks

<a href="/previous-versions/windows/desktop/api/processsnapshot/nf-processsnapshot-psswalksnapshot">PssWalkSnapshot</a> returns a <b>PSS_THREAD_ENTRY</b> structure when the  <a href="/previous-versions/windows/desktop/api/processsnapshot/ne-processsnapshot-pss_walk_information_class">PSS_WALK_INFORMATION_CLASS</a> member that the caller provides it is <b>PSS_WALK_THREADS</b>.

## -see-also

<a href="/previous-versions/windows/desktop/proc_snap/process-snapshotting-portal">Process Snapshotting</a>

