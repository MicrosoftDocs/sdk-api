---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _VSS_PROTECTION_FAULT enumeration


## -description


Defines the set of shadow copy protection faults. A shadow copy protection fault occurs when the VSS service is unable to perform a copy-on-write operation to the shadow copy storage area (also called the diff area).


## -enum-fields




### -field VSS_PROTECTION_FAULT_NONE

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
<li>Delete unused shadow copy storage areas by calling the <a href="https://msdn.microsoft.com/daa23f2c-8342-4387-800a-def5951896ee">IVssDifferentialSoftwareSnapshotMgmt3::DeleteUnusedDiffAreas</a> method.</li>
<li>Increase the shadow copy storage area maximum size for the volume by calling the <a href="https://msdn.microsoft.com/c7773fa8-6b43-46bf-b644-0016b261c080">IVssDifferentialSoftwareSnapshotMgmt::ChangeDiffAreaMaximumSize</a> method or the <a href="https://msdn.microsoft.com/9ba621d5-32ec-4512-a18f-dbdadbd3ff09">IVssDifferentialSoftwareSnapshotMgmt2::ChangeDiffAreaMaximumSizeEx</a> method.</li>
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




<a href="https://msdn.microsoft.com/07257d34-23b1-47bf-b613-f65f5d2a977e">IVssDifferentialSoftwareSnapshotMgmt3::ClearVolumeProtectFault</a>



<a href="https://msdn.microsoft.com/65310c38-9fad-49ed-acf4-dacfa3947130">VSS_PROTECTION_FAULT</a>



<a href="https://msdn.microsoft.com/46cdc46e-fc44-452a-8aae-e47c12deedb4">VSS_VOLUME_PROTECTION_INFO</a>
 

 

