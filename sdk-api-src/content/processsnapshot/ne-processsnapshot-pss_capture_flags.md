---
UID: NE:processsnapshot.__unnamed_enum_2
title: PSS_CAPTURE_FLAGS (processsnapshot.h)
description: Flags that specify what PssCaptureSnapshot captures.helpviewer_keywords: ["PSS_CAPTURE_FLAGS","PSS_CAPTURE_FLAGS enumeration","PSS_CAPTURE_HANDLES","PSS_CAPTURE_HANDLE_BASIC_INFORMATION","PSS_CAPTURE_HANDLE_NAME_INFORMATION","PSS_CAPTURE_HANDLE_TRACE","PSS_CAPTURE_HANDLE_TYPE_SPECIFIC_INFORMATION","PSS_CAPTURE_NONE","PSS_CAPTURE_RESERVED_00000002","PSS_CAPTURE_RESERVED_00000400","PSS_CAPTURE_THREADS","PSS_CAPTURE_THREAD_CONTEXT","PSS_CAPTURE_THREAD_CONTEXT_EXTENDED","PSS_CAPTURE_VA_CLONE","PSS_CAPTURE_VA_SPACE","PSS_CAPTURE_VA_SPACE_SECTION_INFORMATION","PSS_CREATE_BREAKAWAY","PSS_CREATE_BREAKAWAY_OPTIONAL","PSS_CREATE_FORCE_BREAKAWAY","PSS_CREATE_MEASURE_PERFORMANCE","PSS_CREATE_RELEASE_SECTION","PSS_CREATE_USE_VM_ALLOCATIONS","proc_snap.pss_capture_flags","processsnapshot/PSS_CAPTURE_FLAGS","processsnapshot/PSS_CAPTURE_HANDLES","processsnapshot/PSS_CAPTURE_HANDLE_BASIC_INFORMATION","processsnapshot/PSS_CAPTURE_HANDLE_NAME_INFORMATION","processsnapshot/PSS_CAPTURE_HANDLE_TRACE","processsnapshot/PSS_CAPTURE_HANDLE_TYPE_SPECIFIC_INFORMATION","processsnapshot/PSS_CAPTURE_NONE","processsnapshot/PSS_CAPTURE_RESERVED_00000002","processsnapshot/PSS_CAPTURE_RESERVED_00000400","processsnapshot/PSS_CAPTURE_THREADS","processsnapshot/PSS_CAPTURE_THREAD_CONTEXT","processsnapshot/PSS_CAPTURE_THREAD_CONTEXT_EXTENDED","processsnapshot/PSS_CAPTURE_VA_CLONE","processsnapshot/PSS_CAPTURE_VA_SPACE","processsnapshot/PSS_CAPTURE_VA_SPACE_SECTION_INFORMATION","processsnapshot/PSS_CREATE_BREAKAWAY","processsnapshot/PSS_CREATE_BREAKAWAY_OPTIONAL","processsnapshot/PSS_CREATE_FORCE_BREAKAWAY","processsnapshot/PSS_CREATE_MEASURE_PERFORMANCE","processsnapshot/PSS_CREATE_RELEASE_SECTION","processsnapshot/PSS_CREATE_USE_VM_ALLOCATIONS"]
old-location: proc_snap\pss_capture_flags.htm
tech.root: proc_snap
ms.assetid: 6146DDA2-2475-45F8-86F3-65791B10743D
ms.date: 12/05/2018
ms.keywords: PSS_CAPTURE_FLAGS, PSS_CAPTURE_FLAGS enumeration, PSS_CAPTURE_HANDLES, PSS_CAPTURE_HANDLE_BASIC_INFORMATION, PSS_CAPTURE_HANDLE_NAME_INFORMATION, PSS_CAPTURE_HANDLE_TRACE, PSS_CAPTURE_HANDLE_TYPE_SPECIFIC_INFORMATION, PSS_CAPTURE_NONE, PSS_CAPTURE_RESERVED_00000002, PSS_CAPTURE_RESERVED_00000400, PSS_CAPTURE_THREADS, PSS_CAPTURE_THREAD_CONTEXT, PSS_CAPTURE_THREAD_CONTEXT_EXTENDED, PSS_CAPTURE_VA_CLONE, PSS_CAPTURE_VA_SPACE, PSS_CAPTURE_VA_SPACE_SECTION_INFORMATION, PSS_CREATE_BREAKAWAY, PSS_CREATE_BREAKAWAY_OPTIONAL, PSS_CREATE_FORCE_BREAKAWAY, PSS_CREATE_MEASURE_PERFORMANCE, PSS_CREATE_RELEASE_SECTION, PSS_CREATE_USE_VM_ALLOCATIONS, proc_snap.pss_capture_flags, processsnapshot/PSS_CAPTURE_FLAGS, processsnapshot/PSS_CAPTURE_HANDLES, processsnapshot/PSS_CAPTURE_HANDLE_BASIC_INFORMATION, processsnapshot/PSS_CAPTURE_HANDLE_NAME_INFORMATION, processsnapshot/PSS_CAPTURE_HANDLE_TRACE, processsnapshot/PSS_CAPTURE_HANDLE_TYPE_SPECIFIC_INFORMATION, processsnapshot/PSS_CAPTURE_NONE, processsnapshot/PSS_CAPTURE_RESERVED_00000002, processsnapshot/PSS_CAPTURE_RESERVED_00000400, processsnapshot/PSS_CAPTURE_THREADS, processsnapshot/PSS_CAPTURE_THREAD_CONTEXT, processsnapshot/PSS_CAPTURE_THREAD_CONTEXT_EXTENDED, processsnapshot/PSS_CAPTURE_VA_CLONE, processsnapshot/PSS_CAPTURE_VA_SPACE, processsnapshot/PSS_CAPTURE_VA_SPACE_SECTION_INFORMATION, processsnapshot/PSS_CREATE_BREAKAWAY, processsnapshot/PSS_CREATE_BREAKAWAY_OPTIONAL, processsnapshot/PSS_CREATE_FORCE_BREAKAWAY, processsnapshot/PSS_CREATE_MEASURE_PERFORMANCE, processsnapshot/PSS_CREATE_RELEASE_SECTION, processsnapshot/PSS_CREATE_USE_VM_ALLOCATIONS
f1_keywords:
- processsnapshot/PSS_CAPTURE_FLAGS
dev_langs:
- c++
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
- PSS_CAPTURE_FLAGS
targetos: Windows
req.typenames: PSS_CAPTURE_FLAGS
req.redist: 
ms.custom: 19H1
---

# PSS_CAPTURE_FLAGS enumeration


## -description


Flags that specify what <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/processsnapshot/nf-processsnapshot-psscapturesnapshot">PssCaptureSnapshot</a> captures.


## -enum-fields




### -field PSS_CAPTURE_NONE

Capture nothing.


### -field PSS_CAPTURE_VA_CLONE

Capture a snapshot of all cloneable pages in the process. The clone includes all <b>MEM_PRIVATE</b> regions, as well as all sections (<b>MEM_MAPPED</b> and <b>MEM_IMAGE</b>) that are shareable. All Win32 sections created via <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-createfilemappinga">CreateFileMapping</a> are shareable.


### -field PSS_CAPTURE_RESERVED_00000002

(Do not use.)


### -field PSS_CAPTURE_HANDLES

Capture the handle table (handle values only).


### -field PSS_CAPTURE_HANDLE_NAME_INFORMATION

Capture name information for each handle.


### -field PSS_CAPTURE_HANDLE_BASIC_INFORMATION

Capture basic handle information such as <b>HandleCount</b>, <b>PointerCount</b>, <b>GrantedAccess</b>, etc.


### -field PSS_CAPTURE_HANDLE_TYPE_SPECIFIC_INFORMATION

Capture type-specific information for supported object types: <b>Process</b>, <b>Thread</b>, <b>Event</b>, <b>Mutant</b>, <b>Section.</b>


### -field PSS_CAPTURE_HANDLE_TRACE

Capture the handle tracing table.


### -field PSS_CAPTURE_THREADS

Capture thread information (IDs only).


### -field PSS_CAPTURE_THREAD_CONTEXT

Capture the context for each thread.


### -field PSS_CAPTURE_THREAD_CONTEXT_EXTENDED

Capture extended context for each thread (e.g. <b>CONTEXT_XSTATE</b>).


### -field PSS_CAPTURE_RESERVED_00000400

(Do not use.)


### -field PSS_CAPTURE_VA_SPACE

Capture a snapshot of the virtual address space. The VA space is captured as an array of <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-memory_basic_information">MEMORY_BASIC_INFORMATION</a> structures. This flag does not capture the contents of the pages.


### -field PSS_CAPTURE_VA_SPACE_SECTION_INFORMATION

For <b>MEM_IMAGE</b> and <b>MEM_MAPPED</b> regions, dumps the path to the file backing the sections (identical to what <a href="https://docs.microsoft.com/windows/desktop/api/psapi/nf-psapi-getmappedfilenamea">GetMappedFileName</a> returns). For <b>MEM_IMAGE</b> regions, also dumps:

<ul>
<li>
<b>IMAGE_NT_HEADERS.FileHeader.TimeDateStamp</b>

</li>
<li>
<b>IMAGE_NT_HEADERS.OptionalHeader.SizeOfImage</b>

</li>
<li>
<b>IMAGE_NT_HEADERS.OptionalHeader.ImageBase</b>

</li>
<li>
<b>IMAGE_NT_HEADERS.OptionalHeader.CheckSum</b>

</li>
</ul>
The PROCESS_VM_READ access right is required on the process handle.

<div class="alert"><b>Warning</b>  This option is only valid when <b>PSS_CAPTURE_VA_SPACE</b> is specified. </div>
<div> </div>

### -field PSS_CAPTURE_IPT_TRACE


### -field PSS_CREATE_BREAKAWAY_OPTIONAL

The breakaway is optional. If the clone process fails to create as a breakaway, then it is created still inside the job. This flag must be specified in combination with either <b>PSS_CREATE_FORCE_BREAKAWAY</b> and/or <b>PSS_CREATE_BREAKAWAY</b>.


### -field PSS_CREATE_BREAKAWAY

The clone is broken away from the parent process' job. This is equivalent to <a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a> flag <b>CREATE_BREAKAWAY_FROM_JOB</b>.


### -field PSS_CREATE_FORCE_BREAKAWAY

The clone is forcefully broken away the parent process's job. This is only allowed for Tcb-privileged callers.


### -field PSS_CREATE_USE_VM_ALLOCATIONS

The facility should not use the process heap for any persistent or transient allocations. The use of the heap may be undesirable in certain contexts such as creation of snapshots in the exception reporting path (where the heap may be corrupted).


### -field PSS_CREATE_MEASURE_PERFORMANCE

Measure performance of the facility. Performance counters can be retrieved via <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/processsnapshot/nf-processsnapshot-pssquerysnapshot">PssQuerySnapshot</a> with the <b>PSS_QUERY_PERFORMANCE_COUNTERS</b> information class of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/processsnapshot/ne-processsnapshot-pss_query_information_class">PSS_QUERY_INFORMATION_CLASS</a>.


### -field PSS_CREATE_RELEASE_SECTION

The virtual address (VA) clone process does not hold a reference to the underlying image. This will cause functions such as <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-queryfullprocessimagenamea">QueryFullProcessImageName</a> to fail on the VA clone process.

<div class="alert"><b>Important</b>  <p class="note"> This flag has no effect unless <b>PSS_CAPTURE_VA_CLONE</b> is specified.

</div>
<div> </div>

## -remarks



If both <b>PSS_CREATE_FORCE_BREAKAWAY</b> and <b>PSS_CREATE_BREAKAWAY</b> are specified, then <b>PSS_CREATE_FORCE_BREAKAWAY</b> takes precedence.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/proc_snap/process-snapshotting-portal">Process Snapshotting</a>
 

 

