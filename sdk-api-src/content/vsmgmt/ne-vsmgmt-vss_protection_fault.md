---
UID: NE:vsmgmt._VSS_PROTECTION_FAULT
title: VSS_PROTECTION_FAULT (vsmgmt.h)
description: Defines the set of shadow copy protection faults.
helpviewer_keywords: ["*PVSS_PROTECTION_FAULT","VSS_PROTECTION_FAULT","VSS_PROTECTION_FAULT enumeration","VSS_PROTECTION_FAULT_COW_READ_FAILURE","VSS_PROTECTION_FAULT_COW_WRITE_FAILURE","VSS_PROTECTION_FAULT_DESTROY_ALL_SNAPSHOTS","VSS_PROTECTION_FAULT_DIFF_AREA_FULL","VSS_PROTECTION_FAULT_DIFF_AREA_MISSING","VSS_PROTECTION_FAULT_DIFF_AREA_REMOVED","VSS_PROTECTION_FAULT_EXTERNAL_WRITER_TO_DIFF_AREA","VSS_PROTECTION_FAULT_FILE_SYSTEM_FAILURE","VSS_PROTECTION_FAULT_GROW_FAILED","VSS_PROTECTION_FAULT_GROW_TOO_SLOW","VSS_PROTECTION_FAULT_IO_FAILURE","VSS_PROTECTION_FAULT_IO_FAILURE_DURING_ONLINE","VSS_PROTECTION_FAULT_MAPPED_MEMORY_FAILURE","VSS_PROTECTION_FAULT_MEMORY_ALLOCATION_FAILURE","VSS_PROTECTION_FAULT_META_DATA_CORRUPTION","VSS_PROTECTION_FAULT_NONE","base.vss_protection_fault","vsmgmt/VSS_PROTECTION_FAULT","vsmgmt/VSS_PROTECTION_FAULT_COW_READ_FAILURE","vsmgmt/VSS_PROTECTION_FAULT_COW_WRITE_FAILURE","vsmgmt/VSS_PROTECTION_FAULT_DESTROY_ALL_SNAPSHOTS","vsmgmt/VSS_PROTECTION_FAULT_DIFF_AREA_FULL","vsmgmt/VSS_PROTECTION_FAULT_DIFF_AREA_MISSING","vsmgmt/VSS_PROTECTION_FAULT_DIFF_AREA_REMOVED","vsmgmt/VSS_PROTECTION_FAULT_EXTERNAL_WRITER_TO_DIFF_AREA","vsmgmt/VSS_PROTECTION_FAULT_FILE_SYSTEM_FAILURE","vsmgmt/VSS_PROTECTION_FAULT_GROW_FAILED","vsmgmt/VSS_PROTECTION_FAULT_GROW_TOO_SLOW","vsmgmt/VSS_PROTECTION_FAULT_IO_FAILURE","vsmgmt/VSS_PROTECTION_FAULT_IO_FAILURE_DURING_ONLINE","vsmgmt/VSS_PROTECTION_FAULT_MAPPED_MEMORY_FAILURE","vsmgmt/VSS_PROTECTION_FAULT_MEMORY_ALLOCATION_FAILURE","vsmgmt/VSS_PROTECTION_FAULT_META_DATA_CORRUPTION","vsmgmt/VSS_PROTECTION_FAULT_NONE"]
old-location: base\vss_protection_fault.htm
tech.root: base
ms.assetid: 65310c38-9fad-49ed-acf4-dacfa3947130
ms.date: 12/05/2018
ms.keywords: '*PVSS_PROTECTION_FAULT, VSS_PROTECTION_FAULT, VSS_PROTECTION_FAULT enumeration, VSS_PROTECTION_FAULT_COW_READ_FAILURE, VSS_PROTECTION_FAULT_COW_WRITE_FAILURE, VSS_PROTECTION_FAULT_DESTROY_ALL_SNAPSHOTS, VSS_PROTECTION_FAULT_DIFF_AREA_FULL, VSS_PROTECTION_FAULT_DIFF_AREA_MISSING, VSS_PROTECTION_FAULT_DIFF_AREA_REMOVED, VSS_PROTECTION_FAULT_EXTERNAL_WRITER_TO_DIFF_AREA, VSS_PROTECTION_FAULT_FILE_SYSTEM_FAILURE, VSS_PROTECTION_FAULT_GROW_FAILED, VSS_PROTECTION_FAULT_GROW_TOO_SLOW, VSS_PROTECTION_FAULT_IO_FAILURE, VSS_PROTECTION_FAULT_IO_FAILURE_DURING_ONLINE, VSS_PROTECTION_FAULT_MAPPED_MEMORY_FAILURE, VSS_PROTECTION_FAULT_MEMORY_ALLOCATION_FAILURE, VSS_PROTECTION_FAULT_META_DATA_CORRUPTION, VSS_PROTECTION_FAULT_NONE, base.vss_protection_fault, vsmgmt/VSS_PROTECTION_FAULT, vsmgmt/VSS_PROTECTION_FAULT_COW_READ_FAILURE, vsmgmt/VSS_PROTECTION_FAULT_COW_WRITE_FAILURE, vsmgmt/VSS_PROTECTION_FAULT_DESTROY_ALL_SNAPSHOTS, vsmgmt/VSS_PROTECTION_FAULT_DIFF_AREA_FULL, vsmgmt/VSS_PROTECTION_FAULT_DIFF_AREA_MISSING, vsmgmt/VSS_PROTECTION_FAULT_DIFF_AREA_REMOVED, vsmgmt/VSS_PROTECTION_FAULT_EXTERNAL_WRITER_TO_DIFF_AREA, vsmgmt/VSS_PROTECTION_FAULT_FILE_SYSTEM_FAILURE, vsmgmt/VSS_PROTECTION_FAULT_GROW_FAILED, vsmgmt/VSS_PROTECTION_FAULT_GROW_TOO_SLOW, vsmgmt/VSS_PROTECTION_FAULT_IO_FAILURE, vsmgmt/VSS_PROTECTION_FAULT_IO_FAILURE_DURING_ONLINE, vsmgmt/VSS_PROTECTION_FAULT_MAPPED_MEMORY_FAILURE, vsmgmt/VSS_PROTECTION_FAULT_MEMORY_ALLOCATION_FAILURE, vsmgmt/VSS_PROTECTION_FAULT_META_DATA_CORRUPTION, vsmgmt/VSS_PROTECTION_FAULT_NONE'
req.header: vsmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: VSS_PROTECTION_FAULT, *PVSS_PROTECTION_FAULT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VSS_PROTECTION_FAULT
 - vsmgmt/_VSS_PROTECTION_FAULT
 - PVSS_PROTECTION_FAULT
 - vsmgmt/PVSS_PROTECTION_FAULT
 - VSS_PROTECTION_FAULT
 - vsmgmt/VSS_PROTECTION_FAULT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VsMgmt.h
api_name:
 - VSS_PROTECTION_FAULT
---

# VSS_PROTECTION_FAULT enumeration


## -description

Defines the set of shadow copy protection faults. A shadow copy protection fault occurs when the VSS service is unable to perform a copy-on-write operation to the shadow copy storage area (also called the diff area).

## -enum-fields

### -field VSS_PROTECTION_FAULT_NONE:0

No shadow copy protection fault has occurred.

### -field VSS_PROTECTION_FAULT_DIFF_AREA_MISSING

The volume that contains the shadow copy storage area could not be found. Usually this fault means that the volume has not yet arrived in the system.

### -field VSS_PROTECTION_FAULT_IO_FAILURE_DURING_ONLINE

The volume that contains the shadow copy storage area could not be brought online because an I/O  failure occurred.

### -field VSS_PROTECTION_FAULT_META_DATA_CORRUPTION

The shadow copy metadata for the shadow copy storage area has been corrupted.

### -field VSS_PROTECTION_FAULT_MEMORY_ALLOCATION_FAILURE

A memory allocation failure occurred. This could be caused by a temporary low-memory condition that does  not happen again after you clear the fault and restart the shadow copy operation.

### -field VSS_PROTECTION_FAULT_MAPPED_MEMORY_FAILURE

A memory mapping failure occurred. This fault could mean that the  page file is too small, or it could be caused by a low-memory condition.

### -field VSS_PROTECTION_FAULT_COW_READ_FAILURE

A read failure occurred during the copy-on-write operation when data was being copied from the live volume to the shadow copy storage area volume.

### -field VSS_PROTECTION_FAULT_COW_WRITE_FAILURE

A read or write failure occurred during the copy-on-write operation when data was being copied from the live volume to the shadow copy storage area volume. One possible reason is that the shadow copy storage area volume has been removed from the system.

### -field VSS_PROTECTION_FAULT_DIFF_AREA_FULL

This failure means that either the shadow copy storage area is full or the shadow copy storage area volume is full. After clearing the protection fault, you can do one of the following:

<ul>
<li>Delete unused shadow copy storage areas by calling the <a href="/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt3-deleteunuseddiffareas">IVssDifferentialSoftwareSnapshotMgmt3::DeleteUnusedDiffAreas</a> method.</li>
<li>Increase the shadow copy storage area maximum size for the volume by calling the <a href="/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt-changediffareamaximumsize">IVssDifferentialSoftwareSnapshotMgmt::ChangeDiffAreaMaximumSize</a> method or the <a href="/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt2-changediffareamaximumsizeex">IVssDifferentialSoftwareSnapshotMgmt2::ChangeDiffAreaMaximumSizeEx</a> method.</li>
</ul>

### -field VSS_PROTECTION_FAULT_GROW_TOO_SLOW

The size of the shadow copy storage area could not be increased because there was no longer enough space on the shadow copy storage area volume.

### -field VSS_PROTECTION_FAULT_GROW_FAILED

The size of the shadow copy storage area could not be increased.

### -field VSS_PROTECTION_FAULT_DESTROY_ALL_SNAPSHOTS

An unexpected error occurred.

### -field VSS_PROTECTION_FAULT_FILE_SYSTEM_FAILURE

Either the shadow copy storage area files could not be opened or the shadow copy storage area volume could not be mounted because of a file system operation failure.

### -field VSS_PROTECTION_FAULT_IO_FAILURE

A read or write failure occurred on the shadow copy storage area volume.

### -field VSS_PROTECTION_FAULT_DIFF_AREA_REMOVED

The shadow copy storage area volume was removed from the system or could not be accessed for some other reason.

### -field VSS_PROTECTION_FAULT_EXTERNAL_WRITER_TO_DIFF_AREA

Another application attempted to write  to the shadow copy storage area.

### -field VSS_PROTECTION_FAULT_MOUNT_DURING_CLUSTER_OFFLINE

## -see-also

<a href="/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt3-clearvolumeprotectfault">IVssDifferentialSoftwareSnapshotMgmt3::ClearVolumeProtectFault</a>



<a href="/windows/desktop/api/vsmgmt/ne-vsmgmt-vss_protection_fault">VSS_PROTECTION_FAULT</a>



<a href="/windows/desktop/api/vsmgmt/ns-vsmgmt-vss_volume_protection_info">VSS_VOLUME_PROTECTION_INFO</a>
