---
UID: TP:proc_snap
ms.assetid: eb3dbed3-9253-33ab-be65-61f1e4ae4cec
ms.author: windowsdriverdev
ms.date: 05/21/18
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: portal
archived: true
---

# Process Snapshotting



Overview of the Process Snapshotting technology.

To develop Process Snapshotting, you need these headers:

 * [processsnapshot.h](..\processsnapshot\index.md)

For the programming guide, see [Process Snapshotting](https://review.docs.microsoft.com/en-us/win32-test/proc_snap).

## Functions

| Title   | Description   |
| ---- |:---- |
| [PssCaptureSnapshot function](..\processsnapshot\nf-processsnapshot-psscapturesnapshot.md) | Captures a snapshot of a target process. |
| [PssDuplicateSnapshot function](..\processsnapshot\nf-processsnapshot-pssduplicatesnapshot.md) | Duplicates a snapshot handle from one process to another. |
| [PssFreeSnapshot function](..\processsnapshot\nf-processsnapshot-pssfreesnapshot.md) | Frees a snapshot. |
| [PssQuerySnapshot function](..\processsnapshot\nf-processsnapshot-pssquerysnapshot.md) | Queries the snapshot. |
| [PssWalkMarkerCreate function](..\processsnapshot\nf-processsnapshot-psswalkmarkercreate.md) | Creates a walk marker. |
| [PssWalkMarkerFree function](..\processsnapshot\nf-processsnapshot-psswalkmarkerfree.md) | Frees a walk marker created by PssWalkMarkerCreate. |
| [PssWalkMarkerGetPosition function](..\processsnapshot\nf-processsnapshot-psswalkmarkergetposition.md) | Returns the current position of a walk marker. |
| [PssWalkMarkerSeekToBeginning function](..\processsnapshot\nf-processsnapshot-psswalkmarkerseektobeginning.md) | Rewinds a walk marker back to the beginning. |
| [PssWalkMarkerSetPosition function](..\processsnapshot\nf-processsnapshot-psswalkmarkersetposition.md) | Sets the position of a walk marker. |
| [PssWalkSnapshot function](..\processsnapshot\nf-processsnapshot-psswalksnapshot.md) | Returns information from the current walk position and advanced the walk marker to the next position. |

## Structures

| Title   | Description   |
| ---- |:---- |
| [PSS_ALLOCATOR structure](..\processsnapshot\ns-processsnapshot-pss_allocator.md) | Specifies custom functions which the Process Snapshotting functions use to allocate and free the internal walk marker structures. |
| [PSS_AUXILIARY_PAGES_INFORMATION structure](..\processsnapshot\ns-processsnapshot-pss_auxiliary_pages_information.md) | Holds auxiliary pages information returned by PssQuerySnapshot. |
| [PSS_AUXILIARY_PAGE_ENTRY structure](..\processsnapshot\ns-processsnapshot-pss_auxiliary_page_entry.md) | Holds auxiliary page entry information returned by PssWalkSnapshot. |
| [PSS_HANDLE_ENTRY structure](..\processsnapshot\ns-processsnapshot-pss_handle_entry.md) | Holds information about a handle returned by PssWalkSnapshot. |
| [PSS_HANDLE_INFORMATION structure](..\processsnapshot\ns-processsnapshot-pss_handle_information.md) | Holds handle information returned by PssQuerySnapshot. |
| [PSS_HANDLE_TRACE_INFORMATION structure](..\processsnapshot\ns-processsnapshot-pss_handle_trace_information.md) | Holds handle trace information returned by PssQuerySnapshot. |
| [PSS_PERFORMANCE_COUNTERS structure](..\processsnapshot\ns-processsnapshot-pss_performance_counters.md) | Holds performance counters returned by PssQuerySnapshot. |
| [PSS_PROCESS_INFORMATION structure](..\processsnapshot\ns-processsnapshot-pss_process_information.md) | Holds process information returned by PssQuerySnapshot. |
| [PSS_THREAD_ENTRY structure](..\processsnapshot\ns-processsnapshot-pss_thread_entry.md) | Holds thread information returned by PssWalkSnapshotPssWalkSnapshot. |
| [PSS_THREAD_INFORMATION structure](..\processsnapshot\ns-processsnapshot-pss_thread_information.md) | Holds thread information returned by PssQuerySnapshot. |
| [PSS_VA_CLONE_INFORMATION structure](..\processsnapshot\ns-processsnapshot-pss_va_clone_information.md) | Holds virtual address (VA) clone information returned by PssQuerySnapshot. |
| [PSS_VA_SPACE_ENTRY structure](..\processsnapshot\ns-processsnapshot-pss_va_space_entry.md) | Holds the MEMORY_BASIC_INFORMATION returned by PssWalkSnapshot for a virtual address (VA) region. |
| [PSS_VA_SPACE_INFORMATION structure](..\processsnapshot\ns-processsnapshot-pss_va_space_information.md) | Holds virtual address (VA) space information returned by PssQuerySnapshot. |

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [PSS_CAPTURE_FLAGS enumeration](..\processsnapshot\ne-processsnapshot-pss_capture_flags.md) | Flags that specify what PssCaptureSnapshot captures. |
| [PSS_DUPLICATE_FLAGS enumeration](..\processsnapshot\ne-processsnapshot-pss_duplicate_flags.md) | Duplication flags for use by PssDuplicateSnapshot. |
| [PSS_HANDLE_FLAGS enumeration](..\processsnapshot\ne-processsnapshot-pss_handle_flags.md) | Flags to specify what parts of a PSS_HANDLE_ENTRY structure are valid. |
| [PSS_OBJECT_TYPE enumeration](..\processsnapshot\ne-processsnapshot-pss_object_type.md) | Specifies the object type in a PSS_HANDLE_ENTRY structure. |
| [PSS_PROCESS_FLAGS enumeration](..\processsnapshot\ne-processsnapshot-pss_process_flags.md) | Flags that describe a process. |
| [PSS_QUERY_INFORMATION_CLASS enumeration](..\processsnapshot\ne-processsnapshot-pss_query_information_class.md) | Specifies what information PssQuerySnapshot function returns. |
| [PSS_THREAD_FLAGS enumeration](..\processsnapshot\ne-processsnapshot-pss_thread_flags.md) | Flags that describe a thread. |
| [PSS_WALK_INFORMATION_CLASS enumeration](..\processsnapshot\ne-processsnapshot-pss_walk_information_class.md) | Specifies what information the PssWalkSnapshot function returns. |
