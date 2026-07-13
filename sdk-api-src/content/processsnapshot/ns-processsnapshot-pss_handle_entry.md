---
UID: NS:processsnapshot.PSS_HANDLE_ENTRY
title: PSS_HANDLE_ENTRY (processsnapshot.h)
description: Holds information about a handle returned by PssWalkSnapshot.
helpviewer_keywords: ["PSS_HANDLE_ENTRY","PSS_HANDLE_ENTRY structure","proc_snap.pss_handle_entry","processsnapshot/PSS_HANDLE_ENTRY"]
old-location: proc_snap\pss_handle_entry.htm
tech.root: proc_snap
ms.assetid: F56E8C35-949A-4DEE-973F-CF24F6596036
ms.date: 12/05/2018
ms.keywords: PSS_HANDLE_ENTRY, PSS_HANDLE_ENTRY structure, proc_snap.pss_handle_entry, processsnapshot/PSS_HANDLE_ENTRY
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
req.typenames: PSS_HANDLE_ENTRY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PSS_HANDLE_ENTRY
 - processsnapshot/PSS_HANDLE_ENTRY
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
 - PSS_HANDLE_ENTRY
---

# PSS_HANDLE_ENTRY structure


## -description

Holds information about a handle returned by <a href="/previous-versions/windows/desktop/api/processsnapshot/nf-processsnapshot-psswalksnapshot">PssWalkSnapshot</a>.

## -struct-fields

### -field Handle

The handle value.

### -field Flags

Flags that indicate what parts of this structure are valid. For more information, see <a href="/previous-versions/windows/desktop/api/processsnapshot/ne-processsnapshot-pss_handle_flags">PSS_HANDLE_FLAGS</a>.

### -field ObjectType

The type of the object that the handle references. For more information, see <a href="/previous-versions/windows/desktop/api/processsnapshot/ne-processsnapshot-pss_object_type">PSS_OBJECT_TYPE</a>.

### -field CaptureTime

The capture time of this information. For more information, see <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>.

### -field Attributes

Attributes.

### -field GrantedAccess

Reserved for use by the operating system.

### -field HandleCount

Reserved for use by the operating system.

### -field PointerCount

Reserved for use by the operating system.

### -field PagedPoolCharge

Reserved for use by the operating system.

### -field NonPagedPoolCharge

Reserved for use by the operating system.

### -field CreationTime

Reserved for use by the operating system.

### -field TypeNameLength

The length of <b>TypeName</b>, in bytes.

### -field TypeName

The type name of the object referenced by this handle. The buffer may not terminated by a <b>NULL</b> character. The pointer is valid for the lifetime of the walk marker passed to <a href="/previous-versions/windows/desktop/api/processsnapshot/nf-processsnapshot-psswalksnapshot">PssWalkSnapshot</a>.

### -field ObjectNameLength

The length of <b>ObjectName</b>, in bytes.

### -field ObjectName

Specifies the name of the object referenced by this handle. The buffer may not terminated by a <b>NULL</b> character. The pointer is valid for the lifetime of the walk marker passed to <a href="/previous-versions/windows/desktop/api/processsnapshot/nf-processsnapshot-psswalksnapshot">PssWalkSnapshot</a>.

### -field TypeSpecificInformation

Type-specific information.



#### Process

Valid for <b>ObjectType</b> = <b>PSS_OBJECT_TYPE_PROCESS</b>.



##### ExitStatus

The exit code of the process. If the process has not exited, this is set to <b>STILL_ACTIVE</b> (259).



##### PebBaseAddress

The address of the process environment block (PEB). Reserved for use by the operating system.



##### AffinityMask

The affinity mask of the process.



##### BasePriority

The base priority level of the process.



##### ProcessId

The process ID.



##### ParentProcessId

The parent process ID.



##### Flags

Flags about the process. For more information, see <a href="/previous-versions/windows/desktop/api/processsnapshot/ne-processsnapshot-pss_process_flags">PSS_PROCESS_FLAGS</a>.



#### Thread

Valid for <b>ObjectType</b> = <b>PSS_OBJECT_TYPE_THREAD</b>.



##### ExitStatus

The exit code of the process. If the process has not exited, this is set to <b>STILL_ACTIVE</b> (259).



##### TebBaseAddress

The address of the thread environment block (TEB). Reserved for use by the operating system.



##### ProcessId

The process ID.



##### ThreadId

The thread ID.



##### AffinityMask

The affinity mask of the process.



##### Priority

The thread’s dynamic priority level.



##### BasePriority

The thread’s base priority level.



##### Win32StartAddress

A pointer to the thread procedure for the thread.



#### Mutant

Valid for <b>ObjectType</b> = <b>PSS_OBJECT_TYPE_MUTANT</b>.



##### CurrentCount

Reserved for use by the operating system.



##### Abandoned

<b>TRUE</b> if the mutant has been abandoned (the owning thread exited without releasing the mutex), <b>FALSE</b> if not.



##### OwnerProcessId

The process ID of the owning thread, at the time of snapshot creation and handle capture.



##### OwnerThreadId

The process ID of the owning thread, at the time of snapshot creation and handle capture.



#### Event

Valid for <b>ObjectType</b> = <b>PSS_OBJECT_TYPE_EVENT</b>.



##### ManualReset

<b>TRUE</b> if the event is manual reset, <b>FALSE</b> if not.



##### Signaled

<b>TRUE</b> if the event was signaled at the time of snapshot creation and handle capture, <b>FALSE</b> if not.



#### Section

Valid for <b>ObjectType</b> = <b>PSS_OBJECT_TYPE_SECTION</b>.



##### BaseAddress

Reserved for use by the operating system.



##### AllocationAttributes

Reserved for use by the operating system.



##### MaximumSize

Reserved for use by the operating system.

### -field Process

### -field Process.ExitStatus

### -field Process.PebBaseAddress

### -field Process.AffinityMask

### -field Process.BasePriority

### -field Process.ProcessId

### -field Process.ParentProcessId

### -field Process.Flags

### -field Thread

### -field Thread.ExitStatus

### -field Thread.TebBaseAddress

### -field Thread.ProcessId

### -field Thread.ThreadId

### -field Thread.AffinityMask

### -field Thread.Priority

### -field Thread.BasePriority

### -field Thread.Win32StartAddress

### -field Mutant

### -field Mutant.CurrentCount

### -field Mutant.Abandoned

### -field Mutant.OwnerProcessId

### -field Mutant.OwnerThreadId

### -field Event

### -field Event.ManualReset

### -field Event.Signaled

### -field Section

### -field Section.BaseAddress

### -field Section.AllocationAttributes

### -field Section.MaximumSize

### -field Semaphore

### -field Semaphore.CurrentCount

### -field Semaphore.MaximumCount

## -remarks

<a href="/previous-versions/windows/desktop/api/processsnapshot/nf-processsnapshot-psswalksnapshot">PssWalkSnapshot</a> returns a <b>PSS_HANDLE_ENTRY</b> structure when the  <a href="/previous-versions/windows/desktop/api/processsnapshot/ne-processsnapshot-pss_walk_information_class">PSS_WALK_INFORMATION_CLASS</a> member that the caller provides it is <b>PSS_WALK_HANDLES</b>.

## -see-also

<a href="/previous-versions/windows/desktop/proc_snap/process-snapshotting-portal">Process Snapshotting</a>

