---
UID: NS:processsnapshot.__unnamed_struct_10
title: PSS_HANDLE_ENTRY
author: windows-sdk-content
description: Holds information about a handle returned by PssWalkSnapshot.
old-location: proc_snap\pss_handle_entry.htm
tech.root: proc_snap
ms.assetid: F56E8C35-949A-4DEE-973F-CF24F6596036
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PSS_HANDLE_ENTRY, PSS_HANDLE_ENTRY structure, proc_snap.pss_handle_entry, processsnapshot/PSS_HANDLE_ENTRY
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - processsnapshot.h
api_name:
 - PSS_HANDLE_ENTRY
product: Windows
targetos: Windows
req.typenames: PSS_HANDLE_ENTRY
req.redist: 
---

# PSS_HANDLE_ENTRY structure


## -description


Holds information about a handle returned by <a href="https://msdn.microsoft.com/C6AC38B5-0A1C-44D7-A1F6-8196AE9B8FB0">PssWalkSnapshot</a>.


## -struct-fields




### -field Handle

The handle value.


### -field Flags

Flags that indicate what parts of this structure are valid. For more information, see <a href="https://msdn.microsoft.com/A4A604A9-0210-413C-BCAC-F8458B371D42">PSS_HANDLE_FLAGS</a>.


### -field ObjectType

The type of the object that the handle references. For more information, see <a href="https://msdn.microsoft.com/3AF2AE47-6E1A-4B20-B6A3-36C1DDB80674">PSS_OBJECT_TYPE</a>.


### -field CaptureTime

The capture time of this information. For more information, see <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a>.


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

The type name of the object referenced by this handle. The buffer may not terminated by a <b>NULL</b> character. The pointer is valid for the lifetime of the walk marker passed to <a href="https://msdn.microsoft.com/C6AC38B5-0A1C-44D7-A1F6-8196AE9B8FB0">PssWalkSnapshot</a>.


### -field ObjectNameLength

The length of <b>ObjectName</b>, in bytes.


### -field ObjectName

Specifies the name of the object referenced by this handle. The buffer may not terminated by a <b>NULL</b> character. The pointer is valid for the lifetime of the walk marker passed to <a href="https://msdn.microsoft.com/C6AC38B5-0A1C-44D7-A1F6-8196AE9B8FB0">PssWalkSnapshot</a>.


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

Flags about the process. For more information, see <a href="https://msdn.microsoft.com/A1C793DD-EE93-47B6-8EA8-3A45DAD55F2D">PSS_PROCESS_FLAGS</a>.



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




<a href="https://msdn.microsoft.com/C6AC38B5-0A1C-44D7-A1F6-8196AE9B8FB0">PssWalkSnapshot</a> returns a <b>PSS_HANDLE_ENTRY</b> structure when the  <a href="https://msdn.microsoft.com/93A79F7F-2164-4F7A-ADE7-C1655EEFC9BF">PSS_WALK_INFORMATION_CLASS</a> member that the caller provides it is <b>PSS_WALK_HANDLES</b>.




## -see-also




<a href="https://msdn.microsoft.com/1dc6fe86-3f5a-4810-8e93-a0fe309c54ee">Process Snapshotting</a>
 

 

